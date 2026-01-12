# AI-Based-Cyber-Security-Threats-Prediction-AI-Agent

ThreatPredict is a comprehensive, enterprise-grade cybersecurity monitoring and threat intelligence platform. It combines real-time attack visualization, AI-powered threat prediction, and multi-modal security scanning to provide security teams with actionable insights and rapid incident response capabilities.

https://github.com/user-attachments/assets/f9ce6a0c-2516-4ed9-ab89-ff482431af91

  
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
-  Scalable and adaptive security operation


## Architecture 
 ![Image Alt](https://github.com/ashutosh-paswan/AI-Based-Cyber-Security-Threats-Prediction-AI-Agent/blob/e5d34ea0c112d824c799a06b15594c63866d1942/Architecture.png)

 
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

 
## AI Features
Table	Description
threat_doctor_conversations	Chat conversation metadata
threat_doctor_messages	Individual chat messages


## System
 - Table	Description
 - monitoring_status	System monitoring state
 - export_history	Export operation records
 - realtime_logs	System log storage


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
