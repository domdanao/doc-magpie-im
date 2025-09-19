# Payment Request (Invoices)

Magpie Payment Request is the perfect solution for businesses that need a simple, professional way to invoice customers. Create and send invoices in minutes, accept multiple payment methods, and get paid faster with automated tracking and notifications.

## What are Payment Requests?

Payment Requests are professional invoices that you can create and send to customers instantly. They provide a secure, branded payment experience that makes it easy for customers to pay you quickly while giving you complete control over the billing process.

## Key Features

### 🚀 Fast and Easy Invoice Creation
- **Simple invoice setup** - Create professional invoices in minutes
- **Customer information** - Add client details and billing addresses
- **Itemized billing** - Include multiple line items with descriptions
- **Automatic calculations** - Tax, discounts, and totals calculated automatically

### 💳 Multiple Payment Options
- **Credit and debit cards** - Visa, Mastercard, and other major cards
- **Digital wallets** - GCash, Maya, and popular e-wallets
- **Bank transfers** - Direct online banking payments
- **Installment plans** - Flexible payment terms for larger amounts

### 📊 Real-Time Payment Tracking
- **Invoice status** - Track sent, viewed, paid, and overdue invoices
- **Payment notifications** - Instant alerts when customers pay
- **Customer activity** - See when invoices are opened and viewed
- **Centralized dashboard** - Manage all invoices in one place

### 🏦 Seamless Payouts
- **Automatic settlement** - Funds transferred to your account
- **Fast processing** - Quick access to your payments
- **Transaction history** - Detailed records for accounting
- **Payout scheduling** - Choose daily, weekly, or monthly transfers

## Perfect Use Cases

### 💼 Professional Services
- Freelance work and consulting fees
- Legal and accounting services
- Marketing and design projects
- Technical support and maintenance

### 🏥 Healthcare and Wellness
- Medical consultations and treatments
- Therapy and counseling sessions
- Fitness training and coaching
- Beauty and spa services

### 🏗️ Contractors and Trades
- Construction and renovation work
- Plumbing and electrical services
- Home maintenance and repairs
- Equipment rental and services

### 📚 Education and Training
- Tutoring and lesson fees
- Course enrollment and materials
- Workshop and seminar payments
- Educational consulting services

## How to Create Payment Requests

### Method 1: Dashboard Creation
1. **Log into** your Magpie dashboard
2. **Navigate to** Payment Requests section
3. **Click "Create New Invoice"**
4. **Add customer details** (name, email, address)
5. **Enter invoice items** (description, quantity, price)
6. **Set payment terms** (due date, payment methods)
7. **Customize branding** (logo, colors, notes)
8. **Send invoice** via email or share link

### Method 2: API Creation
```javascript
// Create a payment request via API
const paymentRequest = await magpie.paymentRequests.create({
  customer: {
    name: 'Acme Corporation',
    email: 'billing@acme.com',
    address: {
      line1: '123 Business Street',
      city: 'Manila',
      postal_code: '1234',
      country: 'PH'
    }
  },
  line_items: [{
    description: 'Web Development Services',
    quantity: 40,
    unit_amount: 2500,
    tax_rate: 0.12
  }],
  payment_method_types: ['card', 'gcash', 'bank_transfer'],
  currency: 'php',
  due_date: '2024-01-31',
  notes: 'Payment due within 30 days of invoice date'
});

console.log(paymentRequest.invoice_url);
```

## Invoice Customization

### Professional Branding
- **Company logo** and business information
- **Custom colors** and styling
- **Professional templates** for different industries
- **Branded email** notifications
- **Custom footer** with terms and contact info

### Payment Terms
- **Due dates** and payment deadlines
- **Late fees** and penalty calculations
- **Early payment** discounts
- **Partial payments** and installments
- **Currency selection** for international clients

### Line Item Details
- **Detailed descriptions** of services or products
- **Hourly rates** and time tracking
- **Product codes** and SKUs
- **Tax calculations** by item or total
- **Discounts** and promotional pricing

## Customer Payment Experience

### Invoice Delivery
1. **Receive invoice** via email notification
2. **Open secure** payment page
3. **Review invoice** details and line items
4. **Choose payment** method
5. **Complete payment** securely
6. **Get instant** confirmation receipt

### Payment Options
- **One-click payments** for returning customers
- **Saved payment** methods for convenience
- **Mobile-optimized** checkout experience
- **Multi-language** support
- **Currency conversion** for international payments

## Invoice Management

### Status Tracking
- **Draft** - Invoice created but not sent
- **Sent** - Invoice delivered to customer
- **Viewed** - Customer opened the invoice
- **Paid** - Payment completed successfully
- **Overdue** - Payment past due date
- **Cancelled** - Invoice cancelled or voided

### Automated Workflows
- **Payment reminders** for overdue invoices
- **Follow-up emails** for unpaid invoices
- **Receipt generation** after payment
- **Thank you messages** for completed payments
- **Recurring invoices** for subscription services

## Reporting and Analytics

### Financial Insights
- **Revenue tracking** over time periods
- **Payment method** performance
- **Customer payment** behavior
- **Outstanding receivables** management
- **Cash flow** projections

### Business Intelligence
- **Best-paying customers** identification
- **Payment trends** and patterns
- **Invoice conversion** rates
- **Average payment** times
- **Revenue forecasting** tools

## Integration Capabilities

### Accounting Software
- **QuickBooks** integration
- **Xero** synchronization
- **SAP** connectivity
- **Custom ERP** integration
- **Tax reporting** automation

### CRM Systems
- **Salesforce** integration
- **HubSpot** connectivity
- **Customer data** synchronization
- **Sales pipeline** tracking
- **Lead conversion** monitoring

### Webhook Notifications
```javascript
// Handle payment request events
app.post('/webhooks/payment-requests', (req, res) => {
  const event = req.body;

  switch (event.type) {
    case 'payment_request.payment_succeeded':
      // Update customer account
      markInvoicePaid(event.data.object.id);

      // Send receipt
      sendPaymentReceipt(event.data.object);
      break;

    case 'payment_request.payment_failed':
      // Handle failed payment
      notifyPaymentFailure(event.data.object);
      break;
  }
});
```

## Best Practices

### Professional Invoicing
✅ **Clear descriptions** of services or products
✅ **Itemized pricing** with transparent costs
✅ **Professional branding** with company logo
✅ **Payment terms** clearly stated
✅ **Contact information** for questions

### Payment Optimization
✅ **Multiple payment** options for convenience
✅ **Mobile-friendly** invoice design
✅ **Send invoices** promptly after work completion
✅ **Follow up** on overdue payments professionally
✅ **Offer early payment** discounts when possible

### Customer Relations
✅ **Personalized messages** in invoice notes
✅ **Thank customers** for prompt payments
✅ **Provide excellent** customer service
✅ **Maintain consistent** communication
✅ **Be flexible** with payment arrangements

## Advanced Features

### Recurring Invoices
- **Subscription billing** automation
- **Regular service** invoicing
- **Automatic invoice** generation
- **Customer notification** preferences
- **Payment retry** logic

### Multi-Currency Support
- **International invoicing** capabilities
- **Real-time exchange** rates
- **Currency conversion** transparency
- **Local payment** methods by region
- **Tax compliance** by country

### Team Collaboration
- **Multi-user access** with permissions
- **Invoice approval** workflows
- **Team notifications** and alerts
- **Role-based access** control
- **Activity logging** and audit trails

## Getting Started

Ready to streamline your invoicing process? Create your first payment request in the Magpie dashboard and start getting paid faster!

[Create Your First Invoice →](https://dashboard.magpie.com/payment-requests/new)

---

*Need help with invoicing? Contact our support team or explore our [billing documentation](https://docs.magpie.com/billing) for more guidance.*