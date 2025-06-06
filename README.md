# MegaPDF Organization Overview

## 🚀 About MegaPDF

MegaPDF is a comprehensive PDF processing platform that provides powerful PDF manipulation tools through both web interface and REST API. Built with Go and designed for scalability, it offers enterprise-grade PDF operations with user management, billing, and extensive customization options.

## 🏗️ Architecture & Tech Stack

### Backend
- **Language**: Go 1.19+
- **Framework**: Gin (HTTP web framework)
- **Database**: MySQL with GORM ORM
- **Authentication**: JWT tokens + API keys
- **External Tools**: pdfcpu, LibreOffice, Ghostscript, ImageMagick, Tesseract OCR

### Key Components
- RESTful API with Swagger documentation
- Role-based access control (Admin/User)
- Rate limiting and middleware stack
- Background job processing
- File management with automatic cleanup
- Email service integration (SMTP)
- Payment processing (PayPal webhooks)
- OAuth integration (Google)

## 🛠️ Core Features

### PDF Operations
- **Convert**: PDF ↔ DOCX, XLSX, PPTX, Images, Text, HTML
- **Compress**: Optimize file size with configurable quality
- **Merge/Split**: Combine multiple PDFs or extract page ranges
- **Protect/Unlock**: Password protection with permission controls
- **Watermark**: Text, image, or PDF watermarks with positioning
- **Sign**: Digital signature with image/text stamps
- **OCR**: Extract text from scanned documents
- **Rotate**: Page rotation with selective page targeting
- **Edit**: Text extraction and editing capabilities
- **Page Management**: Add page numbers, remove pages

### User Management
- User registration/authentication with email verification
- API key generation and management
- Balance/credit system with free operation quotas
- Usage tracking and analytics
- Transaction history and invoicing

### Admin Dashboard
- User management and role assignment
- Pricing configuration (global + per-operation)
- PDF tools enable/disable controls
- Environment variable management
- Usage statistics and monitoring
- Transaction oversight

## 🔧 Configuration & Deployment

### Environment Variables
```bash
# Database
DB_HOST=localhost
DB_PORT=3306
DB_NAME=megapdf
DB_USER=root
DB_PASSWORD=

# Application
APP_URL=http://localhost:3000
API_URL=http://localhost:8080
JWT_SECRET=your-secret-key
DEBUG=false

# Email (SMTP)
SMTP_HOST=smtp.gmail.com
SMTP_PORT=587
SMTP_USER=your-email@gmail.com
SMTP_PASS=your-app-password
EMAIL_FROM=noreply@mega-pdf.com

# Payment (PayPal)
PAYPAL_CLIENT_ID=your-client-id
PAYPAL_CLIENT_SECRET=your-client-secret
PAYPAL_API_BASE=https://api-m.sandbox.paypal.com

# OAuth (Google)
GOOGLE_CLIENT_ID=your-google-client-id
GOOGLE_CLIENT_SECRET=your-google-client-secret
