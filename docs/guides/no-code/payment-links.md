# Payment Links

Create shareable payment links in seconds—no coding, no setup required. Turn any interaction into a potential payment opportunity with Magpie's flexible Payment Links.

## What are Payment Links?

Payment Links are standalone payment pages that you can create instantly and share anywhere. They're perfect for businesses that want to start selling immediately without building a website or e-commerce platform.

### Key Benefits

✅ **Create in seconds** - No technical knowledge required
✅ **Share anywhere** - Social media, messaging, email, QR codes
✅ **Multiple payment methods** - Cards, wallets, bank transfers
✅ **Real-time inventory** - Automatic stock management
✅ **Instant notifications** - Know immediately when payments are made
✅ **Mobile optimized** - Perfect experience on all devices

## Perfect Use Cases

### 🛍️ Social Commerce
- **Instagram and Facebook** product sales
- **WhatsApp business** transactions
- **TikTok and YouTube** creator monetization
- **Social media** influencer collaborations

### 📧 Direct Sales
- **Email campaigns** with payment links
- **SMS marketing** with instant checkout
- **Personal messaging** for custom orders
- **Customer service** payment collection

### 🎯 Event and Service Sales
- **Event ticket** sales
- **Service booking** payments
- **Consultation fees** collection
- **Workshop and course** enrollment

### 🏪 Quick Retail
- **Pop-up shops** and markets
- **Delivery and pickup** services
- **Custom orders** and commissions
- **Emergency sales** and promotions

## How to Create Payment Links

### Method 1: Dashboard Creation
1. **Log into** your Magpie dashboard
2. **Navigate to** Payment Links section
3. **Click "Create New Link"**
4. **Add product details** (name, price, description)
5. **Upload product images** (optional)
6. **Set inventory quantities** (if applicable)
7. **Choose payment methods** to accept
8. **Customize branding** and colors
9. **Generate and share** your link

### Method 2: API Creation
```javascript
// Create a payment link via API
const paymentLink = await magpie.paymentLinks.create({
  line_items: [{
    name: 'Custom T-Shirt Design',
    amount: 1500,
    quantity: 50,
    description: 'Limited edition design',
    image: 'https://yoursite.com/tshirt.jpg'
  }],
  payment_method_types: ['card', 'gcash', 'maya'],
  currency: 'php',
  allow_adjustable_quantity: true,
  metadata: {
    campaign: 'summer-collection',
    designer: 'artist-name'
  }
});

console.log(paymentLink.url); // Share this URL
```

## Customization Options

### Product Information
- **Product name** and detailed description
- **High-quality images** for visual appeal
- **Pricing** in various currencies
- **Stock quantities** and availability
- **Product variations** (size, color, etc.)

### Payment Configuration
- **Multiple payment methods** for customer choice
- **Currency selection** for international sales
- **Adjustable quantities** for bulk purchases
- **Minimum/maximum** order quantities
- **Shipping and tax** calculations

### Branding and Design
- **Company logo** and business information
- **Brand colors** and styling
- **Custom messages** and descriptions
- **Terms and conditions** links
- **Contact information** display

### Advanced Features
- **Inventory tracking** with automatic updates
- **Expiration dates** for limited-time offers
- **Geographic restrictions** for specific markets
- **Customer data collection** forms
- **Redirect URLs** after purchase

## Sharing Your Payment Links

### Direct Sharing
- **Copy and paste** the link anywhere
- **QR code generation** for easy scanning
- **Short URL** creation for social media
- **Embed codes** for websites and blogs

### Social Media Integration
- **Instagram bio** links and stories
- **Facebook posts** and marketplace
- **Twitter** product announcements
- **TikTok** creator fund monetization
- **YouTube** description links

### Marketing Channels
- **Email marketing** campaigns
- **SMS marketing** messages
- **WhatsApp Business** catalogs
- **Print materials** with QR codes
- **Business cards** and flyers

## Inventory Management

### Stock Tracking
- **Real-time inventory** updates
- **Automatic quantity** reduction after purchases
- **Low stock alerts** and notifications
- **Out-of-stock** automatic disabling
- **Restocking** notifications and management

### Product Variations
- **Multiple sizes** and colors
- **Different pricing** tiers
- **Bundle options** and combinations
- **Seasonal variations** and collections
- **Limited edition** releases

## Payment Processing

### Customer Experience
1. **Click your payment link**
2. **View product details** and images
3. **Select quantity** and variations
4. **Choose payment method**
5. **Complete secure checkout**
6. **Receive instant confirmation**

### Business Benefits
- **Instant payment** collection
- **Automatic inventory** updates
- **Real-time notifications** via email/webhook
- **Customer information** capture
- **Order management** integration

## Analytics and Reporting

### Performance Metrics
- **Click-through rates** and traffic sources
- **Conversion rates** by payment method
- **Revenue tracking** over time
- **Customer demographics** and behavior
- **Geographic distribution** of sales

### Business Intelligence
- **Best-performing products** identification
- **Optimal pricing** strategy insights
- **Customer preferences** analysis
- **Seasonal trends** and patterns
- **Marketing channel** effectiveness

## Best Practices

### Optimizing for Conversions
✅ **High-quality product images** that showcase details
✅ **Clear, compelling** product descriptions
✅ **Competitive pricing** with value proposition
✅ **Multiple payment options** for accessibility
✅ **Trust signals** like security badges and reviews

### Marketing Strategies
✅ **Social proof** through customer testimonials
✅ **Limited-time offers** to create urgency
✅ **Bundle deals** for increased order value
✅ **Seasonal promotions** and discounts
✅ **Influencer collaborations** for wider reach

### Customer Service
✅ **Clear contact information** for support
✅ **Detailed FAQ** section
✅ **Return and refund** policy clarity
✅ **Shipping information** and timelines
✅ **Order tracking** capabilities

## Advanced Features

### Subscription Products
- **Recurring payment** setup
- **Subscription management** portal
- **Automatic billing** cycles
- **Usage-based billing** options
- **Subscription analytics** and retention

### Digital Products
- **Instant delivery** after payment
- **Download links** and access codes
- **License key** generation
- **Digital content** protection
- **Automated fulfillment** workflows

### Services and Bookings
- **Appointment scheduling** integration
- **Service package** options
- **Consultation fee** collection
- **Event ticket** sales
- **Workshop enrollment** and payments

## Integration and Automation

### Webhook Notifications
```javascript
// Handle payment link success
app.post('/webhooks/payment-links', (req, res) => {
  const event = req.body;

  if (event.type === 'payment_link.payment_succeeded') {
    const payment = event.data.object;

    // Fulfill order
    processOrder(payment);

    // Update inventory
    updateInventory(payment.line_items);

    // Send confirmation
    sendConfirmationEmail(payment.customer_email);
  }
});
```

### Third-Party Integration
- **CRM systems** for customer management
- **Inventory management** platforms
- **Email marketing** tools
- **Social media** management
- **Accounting software** integration

---

*Ready to start selling with Payment Links? Create your first payment link in the dashboard and start accepting payments in minutes!*