# Odoo Purchasing Module

This module streamlines the purchase process in Odoo, from creating RFQs to managing vendor bills and purchase orders.

## Features

### Purchase Order Management
- Create and manage **Purchase Orders (POs)** manually or automatically
- Support for **draft, sent, confirmed, received, billed, and cancelled** PO states
- Convert **Requests for Quotation (RFQ)** into confirmed Purchase Orders
- View and track the **status of each order line** (e.g., received quantity vs. ordered)

/home/codetrade/Pictures/Screenshots/readme/rfq.png

### Request for Quotation (RFQ)
- Send RFQs to one or multiple vendors simultaneously
- Compare responses side-by-side to select the best offer
- Auto-generate POs from accepted quotations
- Optional **RFQ approval workflow**

/home/codetrade/Pictures/Screenshots/readme/confirm_rfq.png

### Vendor Management
- Maintain vendor profiles with contact information and payment terms
- Define **vendor pricelists** per product or product category
- Automatically assign vendors based on **lowest price**, **preferred supplier**, or **delivery lead time**

/home/codetrade/Pictures/Screenshots/readme/vendor_profile.png


### Integration with Inventory
- Automatically receive products into inventory upon delivery
- Real-time updates of stock quantities based on PO reception
- Full support for **incoming shipments**, **partial receipts**, and **backorders**

### Reporting & Analysis
- Purchase analysis by vendor, product, category, or time period
- Track delivery delays, invoicing status, and vendor performance
- Customizable purchase dashboards and KPIs

/home/codetrade/Pictures/Screenshots/readme/purchase_analysis.png

### Accounting Integration
- Automatically create vendor bills from received POs
- Link bills to purchase orders and products
- Supports multiple taxes, accounts, and analytic tags
- Integration with Odoo Accounting for end-to-end purchase-to-pay workflows

/home/codetrade/Pictures/Screenshots/readme/vendor_bill.png

### Multi-Currency & Multi-Company Support
- Purchase from vendors in **different currencies**
- Automatically fetch and apply **currency exchange rates**
- Fully isolated or shared vendors, products, and transactions across multiple companies

/home/codetrade/Pictures/Screenshots/readme/multi_currency.png

### Configuration Options
- Define and customize **purchase approval workflows** (single or multi-step)
- Choose **default vendors**, **order lead times**, and **product delivery methods**
- Set **purchase units of measure**, **payment terms**, and **incoterms**

### Extendability
- Easily extendable with custom fields, approval rules, or workflows
- Integrates with:
  - Inventory
  - Accounting
  - Invoicing
  - Analytic Accounting
  - Project (for procurement by project/task)


## Installation

1. Go to the **Apps** section in your Odoo instance.
2. Search for **Purchase**.
3. Click **Install** to activate the module.


---

## ✅ Step 7: Add the `Usage` Section

```markdown
## Usage

After installing the module, you can use it as follows:

### Create a Purchase Order
1. Go to **Purchases** > **Purchase Orders**
2. Click **Create**
3. Select a vendor, add products, quantities, and prices
4. Confirm the order to trigger inventory and accounting actions

### Send an RFQ (Request for Quotation)
1. Go to **Purchases** > **Requests for Quotation**
2. Click **Create**
3. Add products and vendors, then click **Send by Email**
4. Once a quote is accepted, click **Confirm Order**

### Vendor Management
- Go to **Purchases** > **Vendors**
- Create or update vendor contact information, pricelists, and payment terms

### Automated Procurement
- Go to **Inventory** > **Products** > Select a Product
- Set up **Reordering Rules** to trigger automatic purchase orders when stock is low

### Reporting
- Go to **Purchases** > **Reporting**
- Analyze purchases by vendor, product, category, or time period
```


## Configuration

You may need to configure the following to match your business needs:

- **Approval Workflows**:
  - Go to **Settings** > **Users & Companies** > **Users**
  - Enable multi-step approval for specific users/roles

- **Vendor Pricelists**:
  - Go to **Purchases** > **Vendors** > Select Vendor
  - Add pricelist lines under the **Sales & Purchases** tab

- **Taxes and Accounts**:
  - Go to **Accounting** > **Configuration** > **Taxes**
  - Make sure proper taxes are applied to your purchase products

- **Inventory Reordering**:
  - Go to **Inventory** > **Products**
  - Enable **Reordering Rules** for automatic procurement


## Dependencies

This module depends on the following core Odoo modules:

- `base`: Core module required by all others
- `purchase`: Main purchasing engine
- `stock`: Inventory and warehouse management
- `account`: For vendor billing and payment tracking
- `mail`: Enables communication and notifications

Make sure these modules are installed and activated.

---

## Compatibility

The module is compatible with the following Odoo versions:

- ✅ Odoo 16.0
- ✅ Odoo 17.0
- ✅ Odoo 18.0

