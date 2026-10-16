# AI-Powered Customer Support & Service Automation

## 1. Introduction
The AI-Powered Customer Support & Service Automation project uses Salesforce to organize customer support information, automate case assignment, and generate AI-assisted summaries. It aims to reduce repetitive manual work and improve visibility into support cases.

## 2. Project Objectives
- Maintain customer, merchandise, order, and support case records.
- Establish relationships between customers, products, orders, and cases.
- Route cases using Salesforce automation and support queues.
- Generate AI-assisted summaries using Prompt Builder.
- Analyze support cases using reports and dashboards.

## 3. Technology Stack
- Salesforce Lightning Experience
- Salesforce custom objects and fields
- Salesforce Flow Builder
- Salesforce Prompt Builder
- Salesforce Reports and Dashboards
- GitHub for documentation and version tracking

## 4. Data Model

### Customer
Stores customer information.
- Customer Name
- Email
- Phone
- Customer Type

### Merchandise
Stores product information.
- Merchandise Name
- Product Code
- Category
- Warranty (Months)
- Active

### Orders
Stores order information and its related customer and product.
- Order Number
- Order Date
- Status
- Customer (Lookup)
- Product (Lookup)

### User Case
Stores support case information.
- Case Type
- Priority
- Issue Category
- Product (Lookup)
- Order (Lookup)
- AI Summary

## 5. Relationships
- An Order references a Customer.
- An Order references a Merchandise record.
- A User Case references a Merchandise record.
- A User Case references an Order.

These lookup relationships connect support issues with the relevant customer transaction and product.

## 6. Automation
Salesforce flows are used for case assignment and routing. The configured support queues include:
- Damage Support Queue
- Warranty Support Queue

The case assignment logic uses case information to determine the appropriate handling path. Flow activation and successful execution should be verified in the target Salesforce org.

## 7. AI-Assisted Summaries
Salesforce Prompt Builder is configured with a prompt template for the AI Summary field on User Case. The generation feature was tested on a sample case.

AI-generated content should be reviewed by a support user before it is relied on for important decisions.

## 8. Reports and Dashboards
### Customer Support Case Analysis
A report that presents User Case information and supports analysis by priority and other selected fields.

### Customer Support Dashboard
A dashboard that visualizes the report data to make support case information easier to review.

## 9. Testing
Sample records were used to verify:
- Creation of customer and merchandise records.
- Creation of orders linked to customers and products.
- Creation of User Cases linked to orders and products.
- AI Summary generation.
- Report and dashboard display.
- Availability of case assignment flows and support queues.

## 10. Maintenance and Troubleshooting
Administrators should periodically review flow status, execution errors, queue membership, permissions, prompt configuration, and report accuracy.

For failures, inspect the relevant error message, identify the root cause, test corrections safely, and validate the result before deployment.

## 11. Limitations and Future Enhancements
Possible future enhancements include:
- A three-day case reminder flow.
- An approval process for selected cases.
- More detailed service-level reporting.
- Additional security and validation testing.
- Expanded Agentforce capabilities where licensed and supported.

These enhancements should be marked complete only after implementation and testing.

## 12. Conclusion
This project demonstrates how Salesforce custom objects, automation, AI-assisted summaries, and analytics can support a structured customer service workflow. The solution can be extended as support requirements evolve.
