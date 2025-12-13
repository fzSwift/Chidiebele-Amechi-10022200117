# Cloud Application Project - Chidiebele Benjamin Amechi, 10022200117

## Project Documentation Report (PDR)
### A Journey Journal: From Vision to Deployment

Course: CS/IT4131: Cloud Application  
Examination: First Semester 2025/2026  
Submitted to: Godwin Ntow Danso  
Date: 16/12/2025

---

## Table of Contents
- [Chapter 1: The Spark—Mapping My Vision](#chapter-1-the-sparkmapping-my-vision)
- [Chapter 2: Listening and Structuring—From Chaos to Clarity](#chapter-2-listening-and-structuringfrom-chaos-to-clarity)
- [Chapter 3: Building the Blueprint—Layers and Leaps](#chapter-3-building-the-blueprintlayers-and-leaps)
- [Chapter 4: The Twist—Inventing What's Next](#chapter-4-the-twistinventing-whats-next)
- [Chapter 5: Hands-On Hustle—Code, Crashes, and Connections](#chapter-5-hands-on-hustlecode-crashes-and-connections)
- [Chapter 6: Trials and Triumphs—Testing the Waters](#chapter-6-trials-and-triumphstesting-the-waters)
- [References](#references)
- [Appendices](#appendices)

---

## Chapter 1: The Spark—Mapping My Vision
*Date Started: [Current Date]*

### 1.1 Project Overview and Objectives

**Project Title:** EcoGhana Electronics - Sustainable Tech Marketplace

**Project Type:** E-commerce Platform

**Niche:** Ghanaian Eco-Electronics Store

**Primary Objectives:**
1. To develop a fully functional cloud-based e-commerce platform
2. To implement sustainable shopping features (carbon footprint calculator, eco-score for products)
3. To demonstrate full SDLC implementation with cloud deployment
4. To incorporate Ghana-local payment and delivery integrations

**Secondary Objectives:**
1. Implement user authentication and authorization
2. Create admin dashboard for product and order management
3. Integrate with cloud services for scalability
4. Implement responsive design for mobile and desktop

**Unique Selling Points:**
- Carbon footprint calculator for each purchase
- Ghana-specific payment methods (MTN Mobile Money, AirtelTigo Cash)
- Local delivery tracking integration
- Eco-rating system for products

  ![Brainstorm Document](images/chapter1/google-doc-brainstorm.png)
*Figure 1.1: Initial brainstorm session captured in Google Docs

### 1.2 Scope Definition and Stakeholders

**In-Scope:**
- User registration and authentication
- Product browsing and search
- Shopping cart and checkout process
- Order management and tracking
- Admin dashboard for CRUD operations
- Payment gateway integration
- Cloud deployment and CI/CD pipeline

**Out-of-Scope:**
- Physical inventory management
- International shipping logistics
- Advanced AI recommendations (beyond basic)
- Mobile app development (web-only)

**Stakeholder Matrix:**

| Stakeholder | Role | Interest/Needs | My Insight |
|-------------|------|----------------|------------|
| **End Customers** | Primary users | Easy shopping, secure payments, delivery tracking | Through simulated chat: Customers want "buy now, pay later" options and local delivery estimates |
| **Admin/Store Owner** | Platform manager | Product management, order processing, analytics | Needs intuitive dashboard with bulk operations |
| **Delivery Partners** | External service | Integration with their tracking systems | API documentation must be clear and standardized |
| **Payment Providers** | External service | Secure transaction processing | MTN Mobile Money API requires specific authentication flows |
| **Developer (Me)** | System builder | Scalable, maintainable code, clear documentation | Must balance innovation with project timeline constraints |

[Stakeholder Feedback](images/chapter1/whatsapp-stakeholder-chat.png)
*Figure 1.2: WhatsApp conversation with potential customer Sarah gathering requirements 

*Note: See Appendix A for WhatsApp chat screenshot with simulated customer feedback.*

### 1.3 Project Timeline and Resource Allocation

**Timeline Overview:** 10 Days (As per examination requirements)

**Key Milestones:**
1. Day 1-2: Planning & Setup
2. Day 3-4: Design & Architecture
3. Day 5-7: Core Implementation
4. Day 8-9: Testing & Integration
5. Day 10: Deployment & Documentation

**Resource Allocation:**
- **Development Tools:** VS Code, GitHub, Postman, Figma
- **Cloud Services:** Vercel (frontend), Render/Railway (backend), MongoDB Atlas (database)
- **Team:** Solo project (all roles: developer, designer, tester, devops)
- **Budget:** $0 (using free tiers of cloud services)

![Hand-drawn Timeline](images/chapter1/gantt-hand-drawn.jpg)
*Figure 1.3a: Initial hand-drawn project timeline*

![Digital Gantt Chart](images/chapter1/gantt-digital.png)
*Figure 1.3b: Digital Gantt chart created in Google Sheets showing task allocation across 10 days*

## Chapter 2: Listening and Structuring—From Chaos to Clarity
*Date Started: [Current Date]*

### 2.1 Functional and Non-Functional Requirements

#### Functional Requirements (What the system WILL do)

**1. User Management:**
- **FR-001:** Users can register with email, password, and basic info
- **FR-002:** Users can log in/log out securely
- **FR-003:** Users can view and edit their profile
- **FR-004:** Users can reset forgotten passwords via email
- **FR-005:** Users can view their order history

**2. Product Management:**
- **FR-006:** Admins can add/edit/delete products
- **FR-007:** Products display with images, descriptions, prices, and eco-ratings
- **FR-008:** Users can browse products by category (Solar, Energy-efficient, Recycled, etc.)
- **FR-009:** Users can search products by name, category, or description
- **FR-010:** Users can filter products by price range, eco-rating, and availability

**3. Shopping Cart & Checkout:**
- **FR-011:** Users can add/remove products from cart
- **FR-012:** Cart persists between sessions (for logged-in users)
- **FR-013:** Users can proceed to checkout from cart
- **FR-014:** Checkout process collects shipping and payment info
- **FR-015:** Multiple payment methods (Card, MTN Mobile Money, AirtelTigo Cash)

**4. Order Management:**
- **FR-016:** Users can view order status and tracking
- **FR-017:** Admins can update order status (Processing, Shipped, Delivered)
- **FR-018:** System sends email notifications for order updates

**5. Admin Dashboard:**
- **FR-019:** Admins can view sales analytics
- **FR-020:** Admins can manage user accounts
- **FR-021:** Admins can generate sales reports
- **FR-022:** Admins can manage product inventory

**6. Innovative Features:**
- **FR-023:** Carbon footprint calculator for each product
- **FR-024:** Eco-score tracking for users
- **FR-025:** Local delivery estimates based on Ghana regions
- **FR-026:** Product comparison feature

#### Non-Functional Requirements (How the system will PERFORM)

**1. Performance:**
- **NFR-001:** Homepage loads in under 2 seconds
- **NFR-002:** Product search returns results in under 1 second
- **NFR-003:** System supports 100 concurrent users
- **NFR-004:** API response time < 200ms for 95% of requests

**2. Security:**
- **NFR-005:** Passwords stored using bcrypt hashing
- **NFR-006:** JWT tokens expire after 24 hours
- **NFR-007:** HTTPS enforced for all connections
- **NFR-008:** Payment data handled via secure third-party APIs

**3. Usability:**
- **NFR-009:** Mobile-responsive design (works on phones/tablets)
- **NFR-010:** Intuitive navigation (user can find cart in < 3 clicks)
- **NFR-011:** Form validation with helpful error messages
- **NFR-012:** Consistent design language throughout

**4. Reliability & Availability:**
- **NFR-013:** 99% uptime for production environment
- **NFR-014:** Automated daily database backups
- **NFR-015:** Graceful error handling (no blank white screens)

**5. Scalability:**
- **NFR-016:** Horizontal scaling possible for increased load
- **NFR-017:** Cloud-native architecture allowing resource adjustment
- **NFR-018:** CDN for static assets (images, CSS, JS)

### 2.2 Database Design

#### Database Technology Choice: MongoDB Atlas
**Why MongoDB?**
- Document-based structure fits e-commerce data (products with varying attributes)
- Flexible schema allows easy addition of new product types
- Cloud-native with Atlas offering free tier
- Good for hierarchical data (categories, product variants)

#### Core Collections (Tables):

**1. Users Collection:**

{
  _id: ObjectId,
  email: String,
  passwordHash: String,
  firstName: String,
  lastName: String,
  phone: String,
  address: {
    street: String,
    city: String,
    region: String,
    gpsCode: String
  },
  ecoScore: Number,
  createdAt: Date,
  updatedAt: Date,
  isAdmin: Boolean
}

#### **2. Products Collection:**
{
  _id: ObjectId,
  name: String,
  description: String,
  price: Number,
  category: String, // "Solar", "Energy-efficient", "Recycled"
  images: [String], // Array of image URLs
  stockQuantity: Number,
  ecoRating: Number, // 1-5 stars
  carbonFootprint: Number, // kg CO2
  specifications: Object, // Flexible key-value pairs
  createdAt: Date,
  updatedAt: Date
}

#### **3. Orders Collection:**
{
  _id: ObjectId,
  userId: ObjectId,
  items: [
    {
      productId: ObjectId,
      quantity: Number,
      priceAtPurchase: Number
    }
  ],
  totalAmount: Number,
  shippingAddress: Object,
  paymentMethod: String, // "card", "mobile_money", "airteltigo"
  paymentStatus: String, // "pending", "completed", "failed"
  orderStatus: String, // "processing", "shipped", "delivered", "cancelled"
  trackingNumber: String,
  createdAt: Date,
  updatedAt: Date
}

#### **4. Carts Collection:**
{
  _id: ObjectId,
  userId: ObjectId,
  items: [
    {
      productId: ObjectId,
      quantity: Number,
      addedAt: Date
    }
  ],
  createdAt: Date,
  updatedAt: Date
}

#### **5. Categories Collection:**
{
  _id: ObjectId,
  name: String,
  description: String,
  parentCategory: ObjectId, // For sub-categories
  imageUrl: String
}

#### **Relationships:**
One-to-Many: User → Orders (one user, many orders)

One-to-One: User → Cart (one cart per user)

Many-to-Many: Products ←→ Categories (via array references)

One-to-Many: Order → Order Items (embedded documents)

See Figure 2.2 for visual ERD representation.

## Chapter 3: Building the Blueprint—Layers and Leaps
*Date Started: [Date]*

### 3.1 Architecture Overview
*[To be filled with architecture diagrams]*

### 3.2 UI/UX and Integration Design
*[To be filled with wireframes]*

---

## Chapter 4: The Twist—Inventing What's Next
*Date Started: [Date]*

### 4.1 Innovative Features
*[To be filled with mind maps and novel features]*

### 4.2 Implementation of Novelty
*[To be filled with pseudocode and implementation plan]*

---

## Chapter 5: Hands-On Hustle—Code, Crashes, and Connections
*Date Started: [Date]*

### 5.1 Backend Implementation
*[To be filled with Node.js/API implementation]*

### 5.2 Frontend Implementation
*[To be filled with React/Next.js components]*

### 5.3 Real-World Implementation
*[To be filled with integration examples]*

---

## Chapter 6: Trials and Triumphs—Testing the Waters
*Date Started: [Date]*

### 6.1 Testing Strategy
*[To be filled with testing approaches and results]*

### 6.2 Deployment Strategy
*[To be filled with CI/CD and cloud deployment]*

---

## References
*[To be filled with citations]*

## Appendices
*[To be filled with additional documents]*

---

**Note:** This document follows the "Journey Journal" format as required. All images are screenshots from the actual development process, dated and captioned appropriately.
