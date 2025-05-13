# Inventory Management System – Domain Mapping

This document describes the domain entities and use cases for an inventory management system based on a conversation with a domain expert.

## Summary

- [Domain Entities](#domain-entities)
  - [Product](#product)
  - [Inventory](#inventory)
  - [Sale](#sale)
  - [PurchaseOrder](#purchaseorder)
- [Use Cases](#use-cases)
  - [CreateProduct](#createproduct)
  - [TrackProductById](#trackproductbyid)
  - [RegisterSale](#registersale)
  - [MonitorStockLevels](#monitorstocklevels)
  - [ViewInventoryHistory](#viewinventoryhistory)
  - [CreatePurchaseOrder](#createpurchaseorder)
  - [ReceiveAlerts](#receivealerts)
- [Notes](#notes)
- [Author](#author)

## Domain Entities

### Product

Represents an individual item that can be tracked and sold.

**Attributes:**

- `id`: Unique identifier
- `name`: Product name
- `size`: Product size
- `color`: Product color
- `cost`: Unit cost
- `minimumStockLevel`: Minimum quantity before restocking is required

**Behaviors:**

- Can be tracked individually
- Triggers alerts when stock is below minimum
- Appears in sales and inventory history

---

### Inventory

Represents the stock information of all products.

**Attributes:**

- `products`: List of products and their current quantities

**Behaviors:**

- Tracks quantity changes
- Provides historical data (sales, stock levels)
- Supports trend analysis

---

### Sale

Represents a sale of one or more products.

**Attributes:**

- `productId`: ID of the sold product
- `quantity`: Quantity sold
- `timestamp`: Sale date and time

**Behaviors:**

- Reduces stock in inventory
- Adds to sales history

---

### PurchaseOrder

Represents a supplier order created to restock inventory.

**Attributes:**

- `productId`: Product to be restocked
- `quantity`: Amount to be ordered
- `estimatedDelivery`: Supplier's delivery estimate

**Behaviors:**

- Can be created manually or automatically
- Integrates with supplier systems

## Use Cases

### CreateProduct

Registers a new product with all its attributes.

---

### TrackProductById

Retrieves product details and current stock based on its unique ID.

---

### RegisterSale

Processes a product sale:

- Decreases product quantity in inventory
- Adds record to sales history

---

### MonitorStockLevels

Checks stock levels and triggers alerts when below the defined threshold.

---

### ViewInventoryHistory

Allows users to:

- View quantity over time
- Analyze product performance
- Identify trends

---

### CreatePurchaseOrder

Automatically generates purchase orders based on:

- Minimum stock levels
- Sales trends

---

### ReceiveAlerts

Delivers low-stock alerts to users via:

- Email
- In-app notifications

## Notes

- Integration with suppliers is essential for real-time updates on delivery timelines.
- Alerts must be configurable per product.
- History and analytics should support filtering by time period and product type.

## Author

- GitHub - [Felipe Santiago Morais](https://github.com/SantiagoMorais)
- Linkedin - [Felipe Santiago](https://www.linkedin.com/in/felipe-santiago-873025288/)
- Instagram - [@felipe.santiago.morais](https://www.instagram.com/felipe.santiago.morais)
- Email - <a href="mailto:contatofelipesantiago@gmail.com" target="blank">contatofelipesantiago@gmail.com</a>
- <a href="https://api.whatsapp.com/send?phone=5531996951033&text=Hi%2C%20Felipe%21%20I%20got%20your%20contact%20from%20your%20github.">Whatsapp</a>
