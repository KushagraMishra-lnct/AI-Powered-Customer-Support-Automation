# Salesforce Data Model

This diagram shows the main objects and lookup relationships in the AI-Powered Customer Support & Service Automation project.

```mermaid
erDiagram
    CUSTOMER ||--o{ ORDERS : places
    MERCHANDISE ||--o{ ORDERS : contains
    ORDERS ||--o{ USER_CASE : relates_to
    MERCHANDISE ||--o{ USER_CASE : concerns

    CUSTOMER {
        string Customer_Name
        string Email
        string Phone
        string Customer_Type
    }

    MERCHANDISE {
        string Merchandise_Name
        string Product_Code
        string Category
        number Warranty_Months
        boolean Active
    }

    ORDERS {
        string Order_Number
        date Order_Date
        string Status
    }

    USER_CASE {
        string Case_Type
        string Priority
        string Issue_Category
        text AI_Summary
    }
```

## Relationships

- **Customer → Orders:** Orders reference their associated customer.
- **Merchandise → Orders:** Orders reference the merchandise ordered.
- **Orders → User Case:** User Cases reference related orders.
- **Merchandise → User Case:** User Cases reference the affected product.

The diagram represents the intended relationships; the exact number of related records depends on the configured lookup fields and Salesforce data.
