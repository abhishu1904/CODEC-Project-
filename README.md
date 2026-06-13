# SaaS Subscription Management Platform

A scalable platform to manage SaaS subscriptions, plans, and billing with automated invoicing and usage analytics.

## 🎯 Objective

Build a comprehensive SaaS subscription management system with support for multiple subscription tiers, automated billing, detailed usage analytics, and role-based administration.

## 🛠️ Tech Stack

- **Frontend:** Next.js 14 (React, TypeScript)
- **Backend:** Node.js + Express
- **Database:** PostgreSQL
- **Payments:** Stripe API
- **Authentication:** NextAuth.js
- **UI Components:** Shadcn/ui
- **Styling:** Tailwind CSS

## ✨ Features

### 1. Subscription Management
- Multiple subscription plans (Free, Pro, Enterprise)
- Easy plan upgrades/downgrades
- Trial periods support
- Automatic renewal management

### 2. Automated Billing & Invoices
- Stripe integration for payment processing
- Automated billing cycles
- Invoice generation and delivery
- Payment failure handling and retries
- Refund processing

### 3. Usage Analytics Dashboard
- Real-time usage tracking
- API call monitoring
- Storage utilization
- User activity logs
- Custom reporting

### 4. Role-Based Admin Panel
- Admin dashboard
- User management
- Subscription monitoring
- Revenue analytics
- System configuration

## 📁 Project Structure

```
.
├── frontend/                 # Next.js frontend application
├── backend/                  # Node.js/Express API server
├── database/                 # PostgreSQL schemas and migrations
├── docs/                     # Documentation
├── .github/                  # GitHub Actions workflows
├── docker-compose.yml        # Local development setup
├── .env.example              # Environment variables template
└── README.md                 # This file
```

## 🚀 Quick Start

### Prerequisites
- Node.js 18+
- PostgreSQL 14+
- Stripe account
- npm or yarn

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/abhishu1904/CODEC-Project-.git
   cd CODEC-Project-
   ```

2. **Setup environment variables**
   ```bash
   cp .env.example .env.local
   ```

3. **Install dependencies**
   ```bash
   # Frontend
   cd frontend && npm install
   
   # Backend
   cd ../backend && npm install
   ```

4. **Setup database**
   ```bash
   cd ../database
   npm run migrate
   npm run seed
   ```

5. **Start development servers**
   ```bash
   # Terminal 1 - Backend
   cd backend && npm run dev
   
   # Terminal 2 - Frontend
   cd frontend && npm run dev
   ```

6. **Access the application**
   - Frontend: http://localhost:3000
   - Backend API: http://localhost:5000
   - Admin Panel: http://localhost:3000/admin

## 📚 API Documentation

Detailed API documentation is available in `/docs/API.md`

### Key Endpoints

#### Subscriptions
- `GET /api/subscriptions` - List all subscriptions
- `POST /api/subscriptions` - Create new subscription
- `PUT /api/subscriptions/:id` - Update subscription
- `DELETE /api/subscriptions/:id` - Cancel subscription

#### Plans
- `GET /api/plans` - List all plans
- `POST /api/plans` - Create new plan
- `PUT /api/plans/:id` - Update plan

#### Billing
- `GET /api/invoices` - List invoices
- `GET /api/invoices/:id` - Get invoice details
- `POST /api/invoices/:id/send` - Send invoice

#### Usage
- `GET /api/usage/:userId` - Get user usage stats
- `POST /api/usage/:userId/track` - Track usage

#### Admin
- `GET /api/admin/dashboard` - Dashboard metrics
- `GET /api/admin/users` - List all users
- `GET /api/admin/revenue` - Revenue analytics

## 🗄️ Database Schema

Key tables:
- `users` - User accounts
- `subscription_plans` - Available plans
- `subscriptions` - Active subscriptions
- `invoices` - Billing invoices
- `payments` - Payment records
- `usage_logs` - Usage tracking
- `audit_logs` - Admin activity logs

## 🔐 Security

- JWT-based authentication
- Role-based access control (RBAC)
- PCI DSS compliance with Stripe
- SQL injection prevention with parameterized queries
- Rate limiting on API endpoints
- HTTPS enforced in production

## 📊 Monitoring & Logging

- Application logging with Winston
- Error tracking with Sentry
- Performance monitoring
- Database query logging

## 🧪 Testing

```bash
# Run tests
npm run test

# Run tests with coverage
npm run test:coverage
```

## 📦 Deployment

Deployment guides:
- [Vercel (Frontend)](./docs/DEPLOYMENT_FRONTEND.md)
- [Heroku (Backend)](./docs/DEPLOYMENT_BACKEND.md)
- [Docker](./docs/DOCKER.md)

## 🤝 Contributing

1. Create a feature branch
2. Make your changes
3. Write/update tests
4. Submit a pull request

## 📝 License

MIT License - see LICENSE file for details

## 📞 Support

For issues and questions, please create an issue on GitHub.

## 🔗 Resources

- [Stripe Documentation](https://stripe.com/docs)
- [Next.js Documentation](https://nextjs.org/docs)
- [Express Documentation](https://expressjs.com/)
- [PostgreSQL Documentation](https://www.postgresql.org/docs/)
