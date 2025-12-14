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

  *Figure 2.1: Email sent to stakeholder Sarah reviewing requirements (Date: [Today's Date])*
  *Figure 2.2: Hand-drawn use case diagram showing main system interactions*

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

### User Stories
As a Customer, I want to:
- Browse products by category
- Search for specific products
- See product details with eco-rating
- Add products to cart
- Checkout securely
- Track my orders
- View my order history

### As an Admin, I want to:
- Add/edit/delete products
- Manage orders
- View sales analytics
- Manage user accounts

*Figure 2.3: Initial ERD sketch showing entity relationships*
*Figure 2.4: Digital ERD created in Draw.io with version history*
  
## Chapter 3: Building the Blueprint—Layers and Leaps
*Date Started: [Current Date]*

### 3.1 Architecture Overview

#### Architectural Style: Layered (N-Tier) Architecture with Microservices Elements
We're adopting a **cloud-native, layered architecture** that separates concerns and allows independent scaling of components.

**Architecture Layers:**

1. **Presentation Layer (Frontend):**
   - **Technology:** Next.js (React framework)
   - **Hosting:** Vercel (Global CDN)
   - **Responsibilities:** User interface, client-side logic, routing

2. **Application Layer (Backend):**
   - **Technology:** Node.js + Express.js
   - **Hosting:** Render (PaaS)
   - **Responsibilities:** Business logic, API endpoints, authentication

3. **Data Layer:**
   - **Technology:** MongoDB Atlas (Primary database)
   - **Hosting:** MongoDB Cloud
   - **Responsibilities:** Data persistence, query processing

4. **Services Layer (External Integrations):**
   - **Payment Processing:** Paystack API (for Ghana payments)
   - **Email Service:** SendGrid or Nodemailer
   - **Image Storage:** Cloudinary or AWS S3
   - **Analytics:** Google Analytics (frontend)

#### Architecture Diagram Components:



#### Key Architectural Decisions:

1. **Why Layered Architecture?**
   - Clear separation of concerns
   - Easy to maintain and test
   - Can scale layers independently
   - Well-suited for academic project with clear grading criteria

2. **Why Next.js over plain React?**
   - Server-side rendering (SSR) for better SEO (critical for e-commerce)
   - Built-in routing and API routes
   - Excellent Vercel integration for deployment

3. **Why MongoDB over SQL database?**
   - Flexible schema for varying product attributes
   - Document structure matches e-commerce data
   - Easier horizontal scaling
   - Free tier available with MongoDB Atlas

4. **Cloud Services Choice:**
   - **Vercel:** Best-in-class for Next.js, automatic CI/CD
   - **Render:** Simple backend hosting with free tier
   - **MongoDB Atlas:** Managed MongoDB with free 512MB cluster

### 3.2 UI/UX and Integration Design

#### Design Principles:
1. **Mobile-First:** 60% of Ghanaian internet users access via mobile
2. **Simplicity:** Clean, intuitive navigation
3. **Local Context:** Ghanaian colors (green, yellow, red), local payment methods
4. **Accessibility:** WCAG 2.1 AA compliance

#### Wireframe Evolution:

We designed 3 key pages with iterative improvements:

**1. Homepage (Landing Page):**

---

## Chapter 4: The Twist—Inventing What's Next
*Date Started: [Current Date]*

### 4.1 Innovative Features

#### Innovation Philosophy:
Our platform goes beyond traditional e-commerce by integrating **environmental consciousness** with **Ghana-specific technology adoption**. We're not just selling products; we're promoting sustainable living in the Ghanaian context.

#### Core Innovations:

**1. Carbon Footprint Calculator (CFC)**
- **Concept:** Real-time environmental impact calculation for each purchase
- **How it works:** 
  - Each product has a pre-calculated carbon footprint (kg CO2)
  - Calculator aggregates cart items and shipping distance
  - Suggests eco-friendly alternatives for high-impact items
  - Provides visual comparison to everyday activities (e.g., "Equivalent to planting X trees")
- **Unique Aspect:** Ghana-specific emission factors and offset options

**2. Eco-Score Gamification System**
- **Concept:** Turn sustainable shopping into a rewarding game
- **How it works:**
  - Users earn points for eco-friendly purchases
  - Bonus points for recycling old electronics through partner programs
  - Points unlock badges, discounts, and exclusive products
  - Public leaderboard for community engagement
- **Unique Aspect:** Integration with local recycling centers in Accra, Kumasi, Takoradi

**3. Ghana-Specific Delivery Intelligence**
- **Concept:** Smart delivery system accounting for Ghana's unique geography
- **How it works:**
  - GPS-based delivery time estimates using Ghana Post GPS codes
  - Real-time traffic patterns for major cities
  - Integration with local transport networks (trotro routes, etc.)
  - Weather-aware delivery scheduling (rainy season adjustments)
- **Unique Aspect:** Uses OpenStreetMap Ghana data and local knowledge

**4. Mobile Money Payment with Carbon Offset Option**
- **Concept:** Seamless mobile payment with built-in environmental contribution
- **How it works:**
  - Standard MTN Mobile Money/AirtelTigo Cash integration
  - Optional "Add ₵1 to offset carbon" at checkout
  - Transparent reporting on offset projects (tree planting, solar installations)
  - Monthly report showing user's collective impact
- **Unique Aspect:** Partnership with Ghana Forestry Commission for local offset projects

**5. "Eco-Duka" Virtual Storefront for Local Artisans**
- **Concept:** Marketplace within marketplace for local eco-entrepreneurs
- **How it works:**
  - Verified Ghanaian artisans can create micro-stores
  - Tools for inventory management and order processing
  - Training resources for digital business skills
  - Featured spotlight on home page rotation
- **Unique Aspect:** Focus on empowering local sustainability entrepreneurs

#### Mind Map Visualization:

The mind map shows how these innovations interconnect:
- **Central Node:** "EcoGhana Sustainable E-commerce"
- **Primary Branches:** 
  1. Environmental Impact (Carbon Calculator, Eco-Score)
  2. Local Integration (Ghana Delivery, Mobile Money)
  3. Community Building (Eco-Duka, Leaderboards)
- **Secondary Branches:** Technical implementation, user benefits, partnerships

### 4.2 Implementation of Novelty

#### Selected for Implementation: Carbon Footprint Calculator

**Why this feature?**
1. Aligns perfectly with our eco-friendly mission
2. Technically challenging but achievable
3. Provides tangible value to users
4. Differentiates us from competitors

#### Technical Implementation Plan:

**1. Data Collection Layer:**
- Product carbon footprint database
- Shipping emission factors (distance × mode)
- Ghana-specific electricity grid emission factors

**2. Calculation Engine:**
- Real-time aggregation during shopping
- Caching for performance optimization
- Fallback estimates when exact data unavailable

**3. Presentation Layer:**
- Visual dashboard in user profile
- Checkout summary with offset options
- Shareable "impact reports"

**4. Integration Points:**
- Product management system (admin)
- Checkout process
- User profile/analytics

#### Pseudocode for Carbon Calculator:

// PSEUDOCODE: Carbon Footprint Calculator
// File: utils/carbonCalculator.js

CLASS CarbonCalculator:
  PROPERTIES:
    - emissionFactors: Object (product categories → kg CO2 per unit)
    - shippingFactors: Object (region → kg CO2 per km)
    - userLocation: String (Ghana region)

  CONSTRUCTOR(userLocation):
    SET this.userLocation = userLocation
    LOAD emissionFactors from database/cache
    LOAD shippingFactors from config

  METHOD calculateProductFootprint(product, quantity):
    // Get base carbon for product
    baseCarbon = product.carbonFootprint OR 
                 this.emissionFactors[product.category] * product.weight
    
    // Adjust for manufacturing location
    IF product.manufacturedInGhana:
      baseCarbon = baseCarbon * 0.7  // 30% reduction for local production
    
    RETURN baseCarbon * quantity

  METHOD calculateShippingFootprint(products, shippingAddress):
    // Calculate total weight
    totalWeight = SUM(products.map(p => p.weight * p.quantity))
    
    // Get distance from warehouse to destination
    distance = this.calculateDistance(this.warehouseLocation, shippingAddress)
    
    // Select shipping mode (truck, moto, etc.)
    shippingMode = this.determineShippingMode(totalWeight, shippingAddress.region)
    
    // Calculate emissions
    emissionFactor = this.shippingFactors[shippingMode]
    shippingCarbon = distance * emissionFactor * totalWeight
    
    RETURN shippingCarbon

  METHOD calculateTotalFootprint(cartItems, shippingAddress):
    // Product emissions
    productCarbon = 0
    FOR EACH item IN cartItems:
      productCarbon += this.calculateProductFootprint(item.product, item.quantity)
    
    // Shipping emissions
    shippingCarbon = this.calculateShippingFootprint(cartItems, shippingAddress)
    
    // Packaging emissions (fixed per order)
    packagingCarbon = 0.5  // kg CO2 for eco-packaging
    
    totalCarbon = productCarbon + shippingCarbon + packagingCarbon
    
    // Convert to relatable metrics
    equivalentMetrics = this.convertToRelatableMetrics(totalCarbon)
    
    RETURN {
      total: totalCarbon.toFixed(2),
      breakdown: {
        products: productCarbon,
        shipping: shippingCarbon,
        packaging: packagingCarbon
      },
      equivalents: equivalentMetrics,
      offsetCost: this.calculateOffsetCost(totalCarbon)
    }

  METHOD calculateOffsetCost(carbonAmount):
    // Current rate: ₵5 per kg CO2 offset
    rate = 5
    cost = carbonAmount * rate
    
    // Round up to nearest cedi for simplicity
    RETURN Math.ceil(cost)

  METHOD convertToRelatableMetrics(carbonKg):
    // Ghana-specific comparisons
    RETURN {
      treesNeeded: Math.ceil(carbonKg / 21.77),  // One tree absorbs ~21.77kg CO2/year
      phoneCharges: Math.round(carbonKg / 0.006), // Smartphone charge emissions
      troTroKm: Math.round(carbonKg / 0.12)  // Emissions per km in trotro
    }

  METHOD suggestReductions(cartItems):
    suggestions = []
    
    FOR EACH item IN cartItems:
      IF item.product.carbonFootprint > this.thresholds.high:
        // Find lower-carbon alternative
        alternative = this.findAlternative(item.product.category, 
                                          item.product.priceRange)
        IF alternative:
          suggestions.push({
            currentItem: item.product.name,
            alternative: alternative.name,
            carbonReduction: item.product.carbonFootprint - alternative.carbonFootprint,
            priceDifference: alternative.price - item.product.price
          })
    
    RETURN suggestions

  PRIVATE METHOD calculateDistance(fromGPS, toGPS):
    // Using Ghana Post GPS codes or coordinates
    // Simplified for pseudocode - would use Haversine formula
    RETURN approximateDistanceInKm(fromGPS, toGPS)

  PRIVATE METHOD determineShippingMode(weight, region):
    IF weight < 5 AND region IN ["Greater Accra", "Ashanti"]:
      RETURN "moto"  // Motorcycle delivery for light items in urban areas
    ELSE IF weight < 50:
      RETURN "van"   // Small van for medium packages
    ELSE:
      RETURN "truck" // Large truck for heavy items

---

![Innovation Mind Map](images/chapter4/mindmap-hand-drawn.jpg)
*Figure 4.1: Hand-drawn mind map showing interconnected innovative features*

![Digital Mind Map Evolution](images/chapter4/mindmap-excel-v2.png)
*Figure 4.2: Digital mind map in Excel showing feature relationships and development*
![VS Code Implementation](images/chapter4/vscode-carbon-calc.png)
*Figure 4.3: VS Code IDE showing Carbon Calculator implementation with syntax highlighting and terminal*

![API Testing](images/chapter4/postman-api-test.png)
*Figure 4.4: Postman testing the carbon calculation API endpoint with sample cart data*

![Test Results](images/chapter4/terminal-tests.png)
*Figure 4.5: Terminal showing successful test execution for carbon calculator*

![Browser Integration](images/chapter4/devtools-network.png)
*Figure 4.6: Browser Dev Tools Network tab showing carbon API call during checkout*
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
