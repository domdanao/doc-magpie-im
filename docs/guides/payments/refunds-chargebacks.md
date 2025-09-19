# Refunds and Chargebacks

Managing refunds and chargebacks effectively is crucial for maintaining customer satisfaction and protecting your business. Magpie provides comprehensive tools and guidance to handle these situations professionally.

## Refunds

### How Refunds Work

When you process a refund through Magpie:
1. **Refund initiated** through your dashboard or API
2. **Customer notification** sent automatically
3. **Amount refunded** to customer's original payment method
4. **Platform fee retained** by Magpie
5. **Net refund amount** deducted from your next payout

### Processing Refunds

#### Through Dashboard
1. **Navigate to** Payments > Transactions
2. **Find the transaction** you want to refund
3. **Click "Refund"** button
4. **Enter refund amount** (partial or full)
5. **Add refund reason** for your records
6. **Confirm refund** processing

#### Through API
```javascript
// Example: Process full refund
POST /v2/charges/{charge_id}/refund
{
  "amount": 5000, // Optional: for partial refunds
  "reason": "customer_request"
}
```

### Refund Policies

#### Your Refund Policy
As a merchant, you have full control over:
- **Refund timeframes** (30 days, 60 days, etc.)
- **Refund conditions** (unused items, restocking fees)
- **Partial vs full refunds**
- **Return shipping** requirements

#### Magpie's Authority
Magpie reserves the right to issue refunds within **60 days** of purchase for:
- **Fraudulent transactions**
- **Unauthorized charges**
- **Policy violations**
- **Customer protection** cases

### Refund Timeline
- **Immediate**: Refund shows in your dashboard
- **1-3 business days**: Customer sees refund in their account
- **5-10 business days**: Full processing for some payment methods
- **Next payout**: Refund amount deducted from your settlement

## Chargebacks

### What is a Chargeback?

A chargeback occurs when a customer contacts their credit card company to dispute a charge, rather than contacting you directly for a refund. The bank then reverses the transaction and investigates the claim.

### Common Chargeback Reasons

#### 🚨 Fraud
- **Unauthorized use** of credit card
- **Identity theft** or stolen card
- **Account takeover** by fraudster

#### ❓ Unrecognized Charge
- **Business name confusion** on statement
- **Forgotten purchase** by customer
- **Family member** made purchase

#### 📦 Non-Receipt
- **Product not delivered** as promised
- **Service not provided** as described
- **Delayed delivery** beyond expectations

#### 💸 Billing Issues
- **Duplicate charges** on customer's card
- **Incorrect amount** charged
- **Subscription not cancelled** properly

### Chargeback Process

#### 1. Notification
- **Immediate alert** via email and dashboard
- **Chargeback details** and reason code
- **Supporting documentation** requirements
- **Response deadline** (typically 10-14 days)

#### 2. Your Response Options

**Accept the Chargeback:**
- **Full refund** processed to customer
- **₱1,500 dispute fee** deducted from next payout
- **Case closed** with no further action needed

**Challenge the Chargeback:**
- **Gather evidence** to dispute the claim
- **Submit compelling evidence** within deadline
- **Wait for decision** from card network
- **Potential reversal** if evidence is strong

#### 3. Dispute Resolution
- **Bank review** of submitted evidence
- **Card network decision** (30-90 days)
- **Final outcome** communicated to all parties

### Compelling Evidence

To successfully challenge a chargeback, provide:

#### For Fraud Claims
✅ **Customer communication** showing legitimate purchase
✅ **IP address** and geolocation data
✅ **AVS and CVV** verification results
✅ **Previous purchase history** from same customer

#### For Non-Receipt Claims
✅ **Delivery confirmation** and tracking information
✅ **Signed delivery receipts**
✅ **Customer communication** acknowledging receipt
✅ **Service completion** documentation

#### For Billing Disputes
✅ **Clear transaction** records and receipts
✅ **Authorization codes** and processing details
✅ **Customer agreement** to terms and pricing
✅ **Subscription or recurring** billing agreements

### Best Practices for Prevention

#### Clear Communication
✅ **Descriptive business name** on statements
✅ **Clear product descriptions** and terms
✅ **Transparent pricing** and billing
✅ **Easy contact information** for customers

#### Customer Service
✅ **Responsive support** team
✅ **Clear return policy** prominently displayed
✅ **Easy refund process** for legitimate requests
✅ **Order confirmation** emails and updates

#### Delivery and Fulfillment
✅ **Reliable shipping** and delivery tracking
✅ **Proof of delivery** for all orders
✅ **Quality products** as described
✅ **Timely service** delivery

#### Documentation
✅ **Detailed order records**
✅ **Customer communication** logs
✅ **Delivery and service** documentation
✅ **Authorization and approval** records

## Financial Impact

### Refund Costs
- **Platform fee retained** by Magpie
- **Refund amount** deducted from next payout
- **No additional fees** for processing refunds

### Chargeback Costs
- **Original transaction** amount reversed
- **₱1,500 dispute fee** regardless of outcome
- **Potential additional** penalties for high chargeback rates
- **Account review** if chargeback rate exceeds thresholds

### Chargeback Rate Management
Maintain a low chargeback rate to avoid:
- **Account restrictions** or holds
- **Increased processing** fees
- **Additional monitoring** requirements
- **Potential account** suspension

## Monitoring and Reporting

### Dashboard Analytics
- **Chargeback rate** tracking and trends
- **Refund volume** and patterns
- **Dispute success** rates
- **Financial impact** summaries

### Alerts and Notifications
- **Real-time chargeback** notifications
- **Refund processing** confirmations
- **Dispute deadline** reminders
- **Case outcome** updates

## Getting Help

### When to Contact Support
- **Complex dispute** cases requiring guidance
- **High chargeback rates** affecting your account
- **Technical issues** with refund processing
- **Policy questions** or clarifications

### Support Resources
- **Knowledge base** with detailed guides
- **Live chat** support during business hours
- **Email support** at support@magpie.im
- **Account management** for enterprise clients

### Professional Services
For businesses with high transaction volumes:
- **Chargeback management** consulting
- **Fraud prevention** strategy development
- **Process optimization** recommendations
- **Custom reporting** and analytics

---

*Need help managing refunds and chargebacks? Our support team is here to guide you through the process and help protect your business.*