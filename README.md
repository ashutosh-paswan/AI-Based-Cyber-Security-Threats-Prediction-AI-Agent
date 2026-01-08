# AI-Based-Cyber-Security-Threats-Prediction-AI-Agent

ThreatPredict is a comprehensive, enterprise-grade cybersecurity monitoring and threat intelligence platform. It combines real-time attack visualization, AI-powered threat prediction, and multi-modal security scanning to provide security teams with actionable insights and rapid incident response capabilities.

  
## PROJECT STATEMENTS 
- Develop agentic AI systems as tireless guardians of network security  
- Enable autonomous monitoring of network traffic to detect anomalies  
- Provide real-time response to cyber threats without human oversight  
- Reduce the workload of human experts, allowing focus on complex challenges  
- Strengthen the overall organizational security posture and resilience

## Key Features
 - Real-time Threat Monitoring
 - Live Attack Map: Interactive 2D/3D visualization of global cyber attacks
 - Attack Globe: Three.js powered 3D globe showing attack origins and targets
 -  Threat Feed: Real-time stream of security incidents with severity classification
 - Analytics Dashboard: Comprehensive metrics, charts, and trend analysis
 - Blocked Attacks View: Monitor and manage blocked threats


## OUTCOMES 
- 24/7 autonomous monitoring of network traffic  
- Real-time detection and response to cyber threats  
- Reduced workload for human security experts  
- Improved organizational resilience against evolving threats  
- Scalable and adaptive security operation
  

## Architecture 
┌─────────────────────────────────────────────────────────────────────────────────┐
│                              CLIENT LAYER (React SPA)                           │
├─────────────────────────────────────────────────────────────────────────────────┤
│  ┌─────────────┐ ┌─────────────┐ ┌─────────────┐ ┌─────────────┐                │
│  │  Dashboard  │ │  Scanners   │ │  Monitoring │ │  AI Tools   │                │
│  │  ─────────  │ │  ─────────  │ │  ─────────  │ │  ─────────  │                │
│  │ • Stats     │ │ • Website   │ │ • Live Map  │ │ • Threat    │                │
│  │ • Charts    │ │ • API       │ │ • 3D Globe  │ │   Doctor    │                │
│  │ • Alerts    │ │ • QR Code   │ │ • Analytics │ │ • Predict   │                │
│  │ • Actions   │ │ • Static    │ │ • Feed      │ │   ions      │                │
│  └─────────────┘ └─────────────┘ └─────────────┘ └─────────────┘                │
│                                                                                 │
│  ┌──────────────────────────────────────────────────────────────────────────┐   │
│  │                        SHARED COMPONENTS                                 │   │
│  │  AppLayout • ProtectedRoute • Charts • Cards • Tables • Forms            │   │
│  └──────────────────────────────────────────────────────────────────────────┘   │
├─────────────────────────────────────────────────────────────────────────────────┤
│                              STATE MANAGEMENT                                   │
│  ┌──────────────┐  ┌───────────────┐  ┌─────────────────┐                       │
│  │ TanStack     │  │ React Hooks   │  │ Real-time       │                       │
│  │ Query        │  │ (Auth, Stats) │  │ Subscriptions   │                       │
│  └──────────────┘  └───────────────┘  └─────────────────┘                       │
└─────────────────────────────────────────────────────────────────────────────────┘
                                        │
                                        ▼
┌─────────────────────────────────────────────────────────────────────────────────┐
│                            SUPABASE BACKEND                                     │
├─────────────────────────────────────────────────────────────────────────────────┤
│  ┌─────────────────────────────────────────────────────────────────────────┐    │
│  │                         EDGE FUNCTIONS (Deno)                           │    │
│  │  ┌──────────────┐ ┌──────────────┐ ┌──────────────┐ ┌──────────────┐    │    │
│  │  │ scan-website │ │ scan-api     │ │ analyze-qr   │ │ scan-static  │    │    │
│  │  └──────────────┘ └──────────────┘ └──────────────┘ └──────────────┘    │    │
│  │  ┌──────────────┐ ┌──────────────┐ ┌──────────────┐ ┌──────────────┐    │    │
│  │  │threat-doctor │ │ live-threat  │ │ block-entity │ │ export-cloud │    │    │
│  │  │    -chat     │ │   -stream    │ │              │ │              │    │    │
│  │  └──────────────┘ └──────────────┘ └──────────────┘ └──────────────┘    │    │
│  └─────────────────────────────────────────────────────────────────────────┘    │
│                                                                                 │
│  ┌─────────────────────────────────────────────────────────────────────────┐    │
│  │                         POSTGRESQL DATABASE                             │    │
│  │  ┌────────────┐ ┌────────────┐ ┌────────────┐ ┌────────────┐            │    │
│  │  │live_attacks│ │ incidents  │ │ profiles   │ │ user_roles │            │    │
│  │  └────────────┘ └────────────┘ └────────────┘ └────────────┘            │    │
│  │  ┌────────────┐ ┌────────────┐ ┌────────────┐ ┌────────────┐            │    │
│  │  │blocked_*   │ │scan_results│ │audit_logs  │ │threat_doc* │            │    │
│  │  └────────────┘ └────────────┘ └────────────┘ └────────────┘            │    │
│  └─────────────────────────────────────────────────────────────────────────┘    │
│                                                                                 │
│  ┌─────────────────────────────────────────────────────────────────────────┐    │
│  │                         AUTHENTICATION (RLS)                            │    │
│  │  • JWT-based authentication    • Row Level Security policies            │    │
│  │  • Role-based access control   • Secure session management              │    │
│  └─────────────────────────────────────────────────────────────────────────┘    │
└─────────────────────────────────────────────────────────────────────────────────┘
                                        │
                                        ▼
┌─────────────────────────────────────────────────────────────────────────────────┐
│                           EXTERNAL INTEGRATIONS                                 │
│  ┌──────────────┐  ┌──────────────┐  ┌──────────────┐                           │
│  │ Lovable AI   │  │ Gemini API   │  │ Threat Intel │                           │
│  │ Gateway      │  │ (Summaries)  │  │ Feeds        │                           │
│  └──────────────┘  └──────────────┘  └──────────────┘                           │
└─────────────────────────────────────────────────────────────────────────────────┘

┌─────────────────────────────────────────────────────────────────────────────────┐
│                              CLIENT LAYER (React SPA)                           │
├─────────────────────────────────────────────────────────────────────────────────┤
│  ┌─────────────┐ ┌─────────────┐ ┌─────────────┐ ┌─────────────┐                │
│  │  Dashboard  │ │  Scanners   │ │  Monitoring │ │  AI Tools   │                │
│  │  ─────────  │ │  ─────────  │ │  ─────────  │ │  ─────────  │                │
│  │ • Stats     │ │ • Website   │ │ • Live Map  │ │ • Threat    │                │
│  │ • Charts    │ │ • API       │ │ • 3D Globe  │ │   Doctor    │                │
│  │ • Alerts    │ │ • QR Code   │ │ • Analytics │ │ • Predict   │                │
│  │ • Actions   │ │ • Static    │ │ • Feed      │ │   ions      │                │
│  └─────────────┘ └─────────────┘ └─────────────┘ └─────────────┘                │
│                                                                                 │
│  ┌──────────────────────────────────────────────────────────────────────────┐   │
│  │                        SHARED COMPONENTS                                 │   │
│  │  AppLayout • ProtectedRoute • Charts • Cards • Tables • Forms            │   │
│  └──────────────────────────────────────────────────────────────────────────┘   │
├─────────────────────────────────────────────────────────────────────────────────┤
│                              STATE MANAGEMENT                                   │
│  ┌──────────────┐  ┌───────────────┐  ┌─────────────────┐                       │
│  │ TanStack     │  │ React Hooks   │  │ Real-time       │                       │
│  │ Query        │  │ (Auth, Stats) │  │ Subscriptions   │                       │
│  └──────────────┘  └───────────────┘  └─────────────────┘                       │
└─────────────────────────────────────────────────────────────────────────────────┘
                                        │
                                        ▼
┌─────────────────────────────────────────────────────────────────────────────────┐
│                            SUPABASE BACKEND                                     │
├─────────────────────────────────────────────────────────────────────────────────┤
│  ┌─────────────────────────────────────────────────────────────────────────┐    │
│  │                         EDGE FUNCTIONS (Deno)                           │    │
│  │  ┌──────────────┐ ┌──────────────┐ ┌──────────────┐ ┌──────────────┐    │    │
│  │  │ scan-website │ │ scan-api     │ │ analyze-qr   │ │ scan-static  │    │    │
│  │  └──────────────┘ └──────────────┘ └──────────────┘ └──────────────┘    │    │
│  │  ┌──────────────┐ ┌──────────────┐ ┌──────────────┐ ┌──────────────┐    │    │
│  │  │threat-doctor │ │ live-threat  │ │ block-entity │ │ export-cloud │    │    │
│  │  │    -chat     │ │   -stream    │ │              │ │              │    │    │
│  │  └──────────────┘ └──────────────┘ └──────────────┘ └──────────────┘    │    │
│  └─────────────────────────────────────────────────────────────────────────┘    │
│                                                                                 │
│  ┌─────────────────────────────────────────────────────────────────────────┐    │
│  │                         POSTGRESQL DATABASE                             │    │
│  │  ┌────────────┐ ┌────────────┐ ┌────────────┐ ┌────────────┐            │    │
│  │  │live_attacks│ │ incidents  │ │ profiles   │ │ user_roles │            │    │
│  │  └────────────┘ └────────────┘ └────────────┘ └────────────┘            │    │
│  │  ┌────────────┐ ┌────────────┐ ┌────────────┐ ┌────────────┐            │    │
│  │  │blocked_*   │ │scan_results│ │audit_logs  │ │threat_doc* │            │    │
│  │  └────────────┘ └────────────┘ └────────────┘ └────────────┘            │    │
│  └─────────────────────────────────────────────────────────────────────────┘    │
│                                                                                 │
│  ┌─────────────────────────────────────────────────────────────────────────┐    │
│  │                         AUTHENTICATION (RLS)                            │    │
│  │  • JWT-based authentication    • Row Level Security policies            │    │
│  │  • Role-based access control   • Secure session management              │    │
│  └─────────────────────────────────────────────────────────────────────────┘    │
└─────────────────────────────────────────────────────────────────────────────────┘
                                        │
                                        ▼
┌─────────────────────────────────────────────────────────────────────────────────┐
│                           EXTERNAL INTEGRATIONS                                 │
│  ┌──────────────┐  ┌──────────────┐  ┌──────────────┐                           │
│  │ Lovable AI   │  │ Gemini API   │  │ Threat Intel │                           │
│  │ Gateway      │  │ (Summaries)  │  │ Feeds        │                           │
│  └──────────────┘  └──────────────┘  └──────────────┘                           │
└─────────────────────────────────────────────────────────────────────────────────┘


## Data Flow
User Request → React Router → Page Component → Custom Hook → Supabase Client
                                                    │
                    ┌───────────────────────────────┼───────────────────────────────┐
                    │                               │                               │
                    ▼                               ▼                               ▼
            Edge Function                   Database Query                  Real-time
            (scan-*, chat)                  (SELECT/INSERT)                 Subscription
                    │                               │                               │
                    └───────────────────────────────┼───────────────────────────────┘
                                                    │
                                                    ▼
                                            Response/Update
                                                    │
                                                    ▼
                                         UI State Update → Re-render

                                         

## Project Structure

threat-predict/
├── public/                    # Static assets
│   ├── favicon.svg
│   └── robots.txt
├── src/
│   ├── components/           # React components
│   │   ├── ai/              # AI-related components
│   │   │   └── MarkdownMessage.tsx
│   │   ├── dashboard/       # Dashboard widgets
│   │   │   ├── RiskGauge.tsx
│   │   │   ├── StatCard.tsx
│   │   │   ├── ThreatChart.tsx
│   │   │   └── ThreatFeed.tsx
│   │   ├── layout/          # Layout components
│   │   │   └── AppLayout.tsx
│   │   └── ui/              # shadcn/ui components
│   ├── hooks/               # Custom React hooks
│   │   ├── useAuth.ts       # Authentication hook
│   │   ├── useLiveThreatData.ts
│   │   ├── useSecurityStats.ts
│   │   └── useThreatDoctorChat.ts
│   ├── integrations/        # Third-party integrations
│   │   └── supabase/
│   │       ├── client.ts    # Supabase client
│   │       └── types.ts     # Generated types
│   ├── lib/                 # Utility functions
│   │   └── utils.ts
│   ├── pages/               # Page components
│   │   ├── ai/             # AI features
│   │   │   ├── Predictions.tsx
│   │   │   └── ThreatDoctor.tsx
│   │   ├── monitor/        # Monitoring views
│   │   │   ├── Analytics.tsx
│   │   │   ├── BlockedAttacks.tsx
│   │   │   ├── GlobeView.tsx
│   │   │   ├── LiveMap.tsx
│   │   │   └── ThreatFeed.tsx
│   │   ├── scanner/        # Security scanners
│   │   │   ├── APIScanner.tsx
│   │   │   ├── QRScanner.tsx
│   │   │   ├── StaticScanner.tsx
│   │   │   └── WebsiteScanner.tsx
│   │   ├── users/          # User management
│   │   │   └── Roles.tsx
│   │   ├── Auth.tsx
│   │   ├── Dashboard.tsx
│   │   ├── Incidents.tsx
│   │   ├── Landing.tsx
│   │   ├── Settings.tsx
│   │   └── Users.tsx
│   ├── App.tsx              # Main app component
│   ├── index.css            # Global styles
│   └── main.tsx             # Entry point
├── supabase/
│   ├── functions/           # Edge functions
│   │   ├── analyze-qr/
│   │   ├── block-entity/
│   │   ├── export-to-cloud/
│   │   ├── live-threat-stream/
│   │   ├── monitor-control/
│   │   ├── multi-agent-analysis/
│   │   ├── scan-api/
│   │   ├── scan-static/
│   │   ├── scan-website/
│   │   └── threat-doctor-chat/
│   └── config.toml          # Supabase config
├── .env                      # Environment variables
├── tailwind.config.ts       # Tailwind configuration
└── vite.config.ts           # Vite configuration


## AI-Powered Intelligence
 - ThreatDoctor Chat: Interactive AI assistant for security guidance with conversation persistence
 - Threat Predictions: ML-driven analysis anticipating potential breaches
 - Auto-generated Recommendations: Context-aware security suggestions
 - Markdown Rendering: Rich text responses with syntax-highlighted code blocks


## Enterprise Management
 - Role-Based Access Control: Admin, Analyst, Viewer roles
 - User Management: Complete user lifecycle management
 - Audit Logging: Comprehensive activity tracking
 - Export History: Track and manage data exports


## Database Schema
Core Tables
Table	Description
live_attacks	Real-time attack data with geolocation
blocked_attacks	History of blocked attacks
blocked_entities	Blocked IPs/domains
incidents	Security incident records
scan_results	Scanner output storage
threats	Threat intelligence data


## User Management
Table	Description
profiles	User profile information
user_roles	Role assignments (admin/analyst/viewer)
audit_logs	User activity audit trail


## AI Features
Table	Description
threat_doctor_conversations	Chat conversation metadata
threat_doctor_messages	Individual chat messages


## System
 - Table	Description
 - monitoring_status	System monitoring state
 - export_history	Export operation records
 - realtime_logs	System log storage


## Edge Functions
Function	Endpoint	Purpose
threat-doctor-chat	/functions/v1/threat-doctor-chat	AI chat assistant
live-threat-stream	/functions/v1/live-threat-stream	Real-time threat data
scan-website	/functions/v1/scan-website	Website vulnerability scan
scan-api	/functions/v1/scan-api	API security audit
analyze-qr	/functions/v1/analyze-qr	QR code analysis
scan-static	/functions/v1/scan-static	Static file analysis
block-entity	/functions/v1/block-entity	Block IP/domain
monitor-control	/functions/v1/monitor-control	Monitoring state control
export-to-cloud	/functions/v1/export-to-cloud	Data export service
multi-agent-analysis	/functions/v1/multi-agent-analysis	Multi-agent threat analysis

## Security

# Authentication
- JWT-based authentication via Supabase Auth
- Secure session management with auto-refresh
- Protected routes for authenticated users

# Authorization
- Role-based access control (RBAC)
- Three roles: admin, analyst, viewer
- Row Level Security (RLS) policies on all tables

# Data Protection
- All API keys stored as environment variables
- Sensitive operations require admin role
- Comprehensive audit logging

See SECURITY.md for security policy and vulnerability reporting.


## Contributing

Contributions are welcome! Please follow these steps:

 - Fork the repository
 - Create a feature branch (git checkout -b feature/amazing-feature)
 - Commit your changes (git commit -m 'Add amazing feature')
 - Push to the branch (git push origin feature/amazing-feature)

   
## License

This project is licensed under the MIT License - see the LICENSE.txt file for details.

Built with ❤️ for cybersecurity professionals
