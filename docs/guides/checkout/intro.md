# Magpie Checkout

Magpie Checkout is a fully-hosted, secure payment form that provides beautiful, conversion-optimized payment experiences for your customers across all devices.

## What is Magpie Checkout?

Magpie Checkout is **the fastest and easiest way to create beautiful payment experiences for your customers!** It's a pre-built, Magpie-hosted checkout solution that handles the entire payment flow while maintaining your brand identity.

### Key Benefits

✅ **Mobile-First Design** - Responsive across mobile, tablet, and desktop
✅ **Zero Development Time** - Ready to use out of the box
✅ **Bank-Grade Security** - PCI DSS Level 1 compliant
✅ **Global Payment Support** - Multiple payment methods and currencies
✅ **Conversion Optimized** - Designed to maximize completion rates

## Features

### 📱 Responsive Design
- **Mobile-optimized** interface that works perfectly on all screen sizes
- **Touch-friendly** controls and navigation
- **Fast loading** times for improved user experience
- **Consistent branding** across all devices

### 🔒 Advanced Security
- **Two-factor authentication** support
- **3D Secure** integration for card payments
- **End-to-end encryption** for all sensitive data
- **Fraud detection** and prevention
- **PCI compliance** handled automatically

### ✨ Smart Form Features
- **Real-time field validation** with clear error messages
- **Auto-completion** for faster checkout
- **Smart formatting** for card numbers and dates
- **Address validation** and suggestions
- **Multi-language support** for global customers

### 🎨 Customization Options
- **Upload your logo** for brand consistency
- **Choose brand colors** to match your website
- **Custom business information** display
- **Flexible payment method** selection
- **Shipping and billing** address collection

## How It Works

### For Your Customers
1. **Click your payment link** or button
2. **Redirected to Checkout** hosted by Magpie
3. **Enter payment details** in secure form
4. **Complete payment** with chosen method
5. **Redirected back** to your success page

### For Your Business
1. **Create Checkout Session** via dashboard or API
2. **Redirect customers** to the checkout URL
3. **Receive webhook** notifications for payment events
4. **Handle success/failure** redirects
5. **Fulfill orders** based on payment status

## Supported Payment Methods

### Credit and Debit Cards
- **Visa** - Global acceptance
- **Mastercard** - Worldwide processing
- **JCB** - Asia-Pacific focused

### Digital Wallets
- **GCash** - Leading Philippine e-wallet
- **Maya** - Popular digital payment platform
- **Alipay** - Chinese digital wallet
- **WeChat Pay** - Social payment platform
- **UnionPay** - Chinese payment network

### Bank Transfers
- **BPI Online** - Direct bank transfers
- **InstaPay** - Real-time transfers
- **Other Philippine banks** - Wide coverage

## Setup and Configuration

### Dashboard Setup
1. **Log into** your Magpie dashboard
2. **Navigate to** Checkout > Settings
3. **Upload your logo** and set brand colors
4. **Configure payment methods** you want to offer
5. **Set up success/cancel URLs** for redirects
6. **Test your checkout** before going live

### Customization Options

#### Branding
- **Company logo** prominently displayed
- **Primary color** for buttons and accents
- **Secondary color** for highlights
- **Custom business** name and description

#### Payment Configuration
- **Select payment methods** to display
- **Set currency** and pricing display
- **Enable/disable** guest checkout
- **Configure shipping** options

#### Address Collection
- **Billing address** collection (optional/required)
- **Shipping address** collection with validation
- **Address auto-complete** for faster entry
- **International address** support

## Integration Methods

### 1. Quick Integration
Perfect for getting started quickly:

```javascript
// Create checkout session
const session = await magpie.checkout.sessions.create({
  payment_method_types: ['card', 'gcash', 'maya'],
  line_items: [{
    name: 'Product Name',
    amount: 5000,
    quantity: 1,
  }],
  mode: 'payment',
  success_url: 'https://yoursite.com/success',
  cancel_url: 'https://yoursite.com/cancel',
});

// Redirect to checkout
window.location.href = session.payment_url;
```

### 2. Advanced Configuration
For more control over the checkout experience:

```javascript
const session = await magpie.checkout.sessions.create({
  payment_method_types: ['card', 'gcash', 'maya', 'bpi'],
  line_items: [
    {
      name: 'Premium Product',
      amount: 15000,
      quantity: 2,
      description: 'High-quality premium item',
      image: 'https://yoursite.com/product-image.jpg'
    }
  ],
  mode: 'payment',
  currency: 'php',
  customer_email: 'customer@example.com',
  billing_address_collection: 'required',
  shipping_address_collection: {
    allowed_countries: ['PH', 'SG', 'US']
  },
  metadata: {
    order_id: '12345',
    customer_id: 'cus_123'
  },
  success_url: 'https://yoursite.com/success?session_id={CHECKOUT_SESSION_ID}',
  cancel_url: 'https://yoursite.com/cancel',
});
```

## Checkout Modes

### Payment Mode
- **One-time payments** for products and services
- **Immediate capture** of funds
- **Instant confirmation** and fulfillment
- **Most common** use case for e-commerce

### Setup Mode
- **Authorize payment** without immediate capture
- **Capture later** when ready to fulfill
- **Useful for** pre-orders and custom products
- **Card verification** for future payments

### Subscription Mode
- **Recurring payments** setup
- **Save payment method** for future use
- **Subscription management** integration
- **Automatic billing** cycles

## Success and Error Handling

### Success Flow
1. **Payment completed** successfully
2. **Customer redirected** to success URL
3. **Webhook sent** to your endpoint
4. **Order fulfillment** can begin
5. **Customer notification** sent

### Error Handling
- **Clear error messages** for payment failures
- **Retry options** for temporary issues
- **Alternative payment methods** suggested
- **Customer support** contact information

### Webhook Integration
```javascript
// Handle successful payment
app.post('/webhooks/checkout', (req, res) => {
  const event = req.body;

  if (event.type === 'checkout.session.completed') {
    const session = event.data.object;
    // Fulfill the order
    fulfillOrder(session.metadata.order_id);
  }

  res.status(200).send('OK');
});
```

## Testing Your Checkout

### Test Mode
- **Use test API keys** for development
- **Test all payment methods** thoroughly
- **Verify webhook** delivery and handling
- **Test success/cancel** redirect flows
- **Check mobile responsiveness**

### Test Cards
Use these test card numbers:
- **4242 4242 4242 4242** - Visa (Success)
- **4000 0000 0000 0002** - Visa (Declined)
- **5555 5555 5555 4444** - Mastercard (Success)
- **4000 0000 0000 9995** - Visa (Insufficient funds)

## Best Practices

### Optimization Tips
✅ **Clear product descriptions** and pricing
✅ **Multiple payment options** for flexibility
✅ **Mobile-friendly** checkout flow
✅ **Trust signals** like security badges
✅ **Progress indicators** for multi-step flows

### Conversion Optimization
✅ **Minimize form fields** where possible
✅ **Guest checkout** option available
✅ **Express payment** methods prominent
✅ **Clear error messaging** and recovery
✅ **Fast loading** times across devices

---

*Ready to implement Magpie Checkout? Start with our quick integration guide or explore our API documentation for advanced customization options.*