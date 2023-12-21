# Create Order Feed

Frank and Oak uses a custom create order file from HotWax that is slightly different than the out of the box used with the native NetSuite integration. Frank and Oak has their own trasnformation middleware in a platform called Boomi that has the business logic for how the order needs to be entered into NetSuite.

Here is a sample of the CSV generated by HotWax

| Header              | Description                                                     |
|---------------------|-----------------------------------------------------------------|
| Order Id            | Shopify Order Name                                              |
| Order Line Id       | HotWax Line ID                                                  |
| External Id         | HotWax Order ID                                                 |
| Sales Channel       | Channel through which the sale was made (e.g., web, POS, etc.)  |
| NetSuite ID         | NetSuite system generated                                       |
| Item                | NetSuite ID of the product being ordered                         |
| External Item ID    | Shopify ID of the product being ordered / Name of discount      |
| Currency            | Currency in which the order is placed                            |
| Price               | **Order Item Price?**                                           |
| Amount              | Total amount for the line item (price * quantity)                |
| Quantity            | Quantity of the item ordered. Always 1 since explode items is enabled |
| Shipping Method     | NetSuite Method ID (e.g., STANDARD_UPS)                          |
| Shipping Cost       | Cost associated with shipping                                   |
| Tax Code            | Code for tax calculation purposes. Vertex for FaO                |
| Shipping Tax Code   | Will include the actual shipping amount from the order           |
| Date                | Date and time when the order was placed                          |
| Customer            | Customer's name                                                 |
| Addressee           | Customer's name for shipping purposes                            |
| Address 1           | Address line 1 for shipping                                      |
| Address 2           | Address line 2 for shipping                                      |
| City                | City for the shipping address                                    |
| State               | State for the shipping address                                   |
| Country             | Country for the shipping address                                 |
| Zip                 | ZIP or postal code for the shipping address                      |
| Email               | Customer's email address from the order                          |
| Phone               | Customer's phone number from the order                          |
| Tag                 | Tag associated with the order                                    |
| Closed              | Indicates whether the order is closed or not. Will be empty in the created feed |
| Discount Item       | Name of the order level discount                                 |
| Rate                | Discount rate applied to the order                               |
| Demand Location     | Location where the order was placed from. Web is set to warehouse |
| Price Level         | Always set to 'Custom'                                           |
| Billing Addressee   | Customer's name for billing purposes                              |
| Billing Address1    | Billing address line 1                                          |
| Billing Address 2   | Billing address line 2                                          |
| Billing City        | City for the billing address                                     |
| Billing State       | State for the billing address                                    |
| Billing Country     | Country for the billing address                                  |
| Billing Zip         | ZIP or postal code for the billing address                       |
| Billing Phone       | Phone number for billing contact                                  |
| Billing Email       | Email address for billing contact                                 |
