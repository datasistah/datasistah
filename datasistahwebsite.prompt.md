# Website Development Prompt: Data Sistah - AI Development & Data Science Services
Using Microsoft official Web Search for Copilot extenstion.

## Project Overview
Create a modern, sleek website for **Data Sistah** (Tiffany Teasley) - an AI Developer, Consultant, and Career Coach. This should replicate the architectural excellence of the AITeach Pro website but with a completely different focus on AI development and data science services.

**IMPORTANT**: Research and add comprehensive AI development resources, tools, guides, and information that would be valuable to customers seeking AI development services. Think about what information, resources, and educational content would help potential clients understand AI development and make informed decisions.

## Design Requirements

### Visual Theme
- **Dark mode aesthetic** with **hot pink accents** (#FF1493, #FF69B4)
- **Modern gradient backgrounds** with subtle animations
- **Bold typography hierarchy** using Google Fonts (Inter recommended)
- **Professional photography integration** - high-quality images of Tiffany throughout

### Technology Stack
- **HTML5**: Semantic markup with proper accessibility
- **CSS3**: Flexbox, Grid, custom properties, keyframe animations
- **JavaScript**: Interactive features, smooth scrolling, mobile navigation
- **Font Awesome 6.0+**: Professional icons throughout
- **Google Fonts**: Inter typography for readability
- **Security**: HTTPS enforcement, security headers, CSP implementation

## Architecture Pattern

### File Structure
```
/
├── index.html (homepage with hero)
├── about.html (Tiffany's story & credentials)
├── ai-development.html (custom AI/web services)
├── coaching.html (career coaching services)
├── speaking.html (speaking engagements)
├── webinar.html (free webinar content)
├── resources.html (AI development resources & guides)
├── portfolio.html (showcase of AI projects)
├── blog.html (AI insights & tutorials)
├── styles.css (complete styling system)
├── script.js (all interactive functionality)
├── images/ (professional photos of Tiffany)
├── vercel.json (deployment configuration with security headers)
└── .github/prompts/ (documentation and prompts)
```

### Responsive Design System
- **Mobile-first approach** with breakpoints: 480px, 768px, 1024px, 1200px
- **Touch-optimized** buttons and navigation
- **Hamburger menu** for mobile with smooth animations
- **Performance optimizations** for mobile devices
- **HTTPS enforcement** with security headers and CSP policies

## Security Requirements

### HTTPS & Security Headers
All pages must be served over HTTPS with comprehensive security headers:

```json
{
  "headers": [
    {
      "source": "/(.*)",
      "headers": [
        {
          "key": "Strict-Transport-Security",
          "value": "max-age=31536000; includeSubDomains; preload"
        },
        {
          "key": "X-Content-Type-Options",
          "value": "nosniff"
        },
        {
          "key": "X-Frame-Options",
          "value": "DENY"
        },
        {
          "key": "X-XSS-Protection",
          "value": "1; mode=block"
        },
        {
          "key": "Referrer-Policy",
          "value": "strict-origin-when-cross-origin"
        },
        {
          "key": "Content-Security-Policy",
          "value": "default-src 'self'; script-src 'self' 'unsafe-inline' cdnjs.cloudflare.com; style-src 'self' 'unsafe-inline' fonts.googleapis.com cdnjs.cloudflare.com; font-src 'self' fonts.gstatic.com; img-src 'self' data:; connect-src 'self'"
        }
      ]
    }
  ]
}
```

### HTML Security Meta Tags
Every HTML page must include security meta tags in the `<head>` section:

```html
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="Content-Security-Policy" content="upgrade-insecure-requests">
    <meta name="referrer" content="strict-origin-when-cross-origin">
    <title>Page Title</title>
    <!-- Other meta tags and links -->
</head>
```

### Security Features Implementation
- **HTTPS Enforcement**: All HTTP requests automatically redirect to HTTPS
- **HSTS Header**: Prevents downgrade attacks and cookie hijacking
- **CSP Policy**: Prevents XSS attacks and unauthorized resource loading
- **Frame Protection**: Prevents clickjacking attacks
- **Content Type Protection**: Prevents MIME type sniffing attacks
- **XSS Protection**: Browser-level XSS filtering enabled
- **Referrer Policy**: Controls referrer information sent to external sites

## Content Structure & Research Requirements

### 1. Hero Section (index.html)
```html
<!-- Hero with dark background, pink gradients -->
<section class="hero">
    <div class="hero-content">
        <h1>Data Sistah</h1>
        <p class="tagline">From Classroom to Code – Let's Build What's Next</p>
        <div class="hero-stats">
            <div class="stat">
                <span class="stat-number">500+</span>
                <span class="stat-label">AI Projects Delivered</span>
            </div>
            <div class="stat">
                <span class="stat-number">100+</span>
                <span class="stat-label">Clients Transformed</span>
            </div>
            <div class="stat">
                <span class="stat-number">20+</span>
                <span class="stat-label">Years Experience</span>
            </div>
        </div>
        <div class="cta-buttons">
            <a href="#portfolio" class="btn-primary">Amplify Your Portfolio with AI</a>
            <a href="#coaching" class="btn-secondary">Book 1:1 Coaching Session</a>
            <a href="#webinar" class="btn-accent">Free Career Webinar</a>
        </div>
    </div>
    <div class="hero-image">
        <img src="images/tiffany-hero.jpg" alt="Tiffany Teasley - Data Sistah">
    </div>
</section>
```

### 2. About Section Structure
**Research & Include:**
- **Professional journey**: 20 years teaching → tech pivot → AI developer
- **Credentials & Recognition**: LinkedIn Top Voice, NY Times Square Billboard, speaking engagements
- **Technical expertise**: Specific AI technologies, programming languages, frameworks
- **Mission statement**: Helping others break into tech authentically
- **High-quality photo**: Casual, confident shot of Tiffany
- **Client success metrics**: Job placement rates, portfolio improvement stats

### 3. AI Development Services Architecture

#### **Research Required**: Add comprehensive information about:

**Custom AI Solutions Section:**
- **Machine Learning Models**: Predictive analytics, recommendation systems, NLP models
- **AI-Powered Websites**: Chatbots, personalization engines, automated content generation
- **Data Science Projects**: Data visualization, statistical analysis, business intelligence
- **AI Consulting**: Strategy development, tool selection, implementation planning
- **Training & Workshops**: Team training on AI tools, custom curriculum development

```html
<section class="ai-services-grid">
    <div class="service-card featured">
        <i class="fas fa-robot"></i>
        <h3>Custom AI Solutions</h3>
        <p>End-to-end AI development from concept to deployment</p>
        <ul class="service-features">
            <li>Machine Learning Models</li>
            <li>Natural Language Processing</li>
            <li>Computer Vision Applications</li>
            <li>Predictive Analytics</li>
        </ul>
        <div class="pricing">Starting at $5,000</div>
        <a href="#contact" class="btn-service">Get Started</a>
    </div>
    
    <div class="service-card">
        <i class="fas fa-globe"></i>
        <h3>AI-Powered Websites</h3>
        <p>Modern websites with integrated AI features - built in hours, not weeks</p>
        <ul class="service-features">
            <li>Intelligent Chatbots</li>
            <li>Content Personalization</li>
            <li>Automated SEO Optimization</li>
            <li>Real-time Analytics</li>
        </ul>
        <div class="pricing">Starting at $2,500</div>
        <a href="#contact" class="btn-service">Learn More</a>
    </div>
    
    <div class="service-card">
        <i class="fas fa-chart-line"></i>
        <h3>Data Science Consulting</h3>
        <p>Transform your data into actionable business insights</p>
        <ul class="service-features">
            <li>Data Analysis & Visualization</li>
            <li>Business Intelligence Dashboards</li>
            <li>Statistical Modeling</li>
            <li>Performance Optimization</li>
        </ul>
        <div class="pricing">Starting at $3,000</div>
        <a href="#contact" class="btn-service">Explore Options</a>
    </div>
</section>
```

### 4. Career Coaching Services
**Research & Add:**
- **Portfolio Development**: Before/after examples, industry standards
- **Interview Preparation**: Technical interview guides, coding challenges
- **Skill Assessment**: Gap analysis, learning roadmaps
- **Industry Insights**: Salary data, job market trends, hiring patterns
- **Networking Strategies**: LinkedIn optimization, community building

```html
<section class="coaching-services">
    <div class="coaching-options">
        <div class="coaching-card">
            <h3>1:1 Coaching</h3>
            <p>Personalized career strategy and portfolio development</p>
            <div class="coaching-features">
                <span class="feature">✓ Resume & LinkedIn Optimization</span>
                <span class="feature">✓ Portfolio Review & Enhancement</span>
                <span class="feature">✓ Interview Preparation</span>
                <span class="feature">✓ Salary Negotiation Coaching</span>
            </div>
            <div class="pricing">$150/hour</div>
        </div>
        
        <div class="coaching-card featured">
            <h3>AMPLIFY Your Portfolio</h3>
            <p>Live portfolio revamp using AI tools and modern design</p>
            <div class="coaching-features">
                <span class="feature">✓ Real-time Development Session</span>
                <span class="feature">✓ AI-Enhanced Projects</span>
                <span class="feature">✓ Modern Design Implementation</span>
                <span class="feature">✓ Deployment & Optimization</span>
            </div>
            <div class="pricing">$500/session</div>
        </div>
    </div>
</section>
```

### 5. AI Development Resources Section (NEW)

**Research & Create Comprehensive Resources:**

#### **AI Development Tools & Frameworks**
- **Programming Languages**: Python, R, JavaScript, Julia
- **ML Libraries**: TensorFlow, PyTorch, scikit-learn, Keras
- **AI Platforms**: OpenAI API, Google Cloud AI, AWS SageMaker, Azure ML
- **Development Tools**: Jupyter Notebooks, Google Colab, VS Code extensions
- **Deployment Platforms**: Heroku, Vercel, AWS, Google Cloud

#### **Learning Resources**
- **Free Courses**: Coursera, edX, Udacity AI/ML courses
- **Documentation**: Official docs for major AI frameworks
- **Tutorials**: Step-by-step guides for common AI implementations
- **Code Examples**: GitHub repositories with practical AI projects
- **Datasets**: Public datasets for practice and learning

#### **Industry Insights**
- **Market Trends**: Current AI adoption rates, emerging technologies
- **Career Paths**: Different roles in AI/ML, skill requirements
- **Salary Information**: Compensation ranges for AI professionals
- **Job Market**: Demand statistics, growth projections

```html
<section class="resources-hub">
    <div class="resource-categories">
        <div class="resource-card">
            <i class="fas fa-code"></i>
            <h3>Development Tools</h3>
            <p>Essential tools and frameworks for AI development</p>
            <a href="resources.html#tools" class="resource-link">Explore Tools →</a>
        </div>
        
        <div class="resource-card">
            <i class="fas fa-graduation-cap"></i>
            <h3>Learning Resources</h3>
            <p>Curated courses, tutorials, and documentation</p>
            <a href="resources.html#learning" class="resource-link">Start Learning →</a>
        </div>
        
        <div class="resource-card">
            <i class="fas fa-chart-bar"></i>
            <h3>Industry Insights</h3>
            <p>Market trends, salary data, and career guidance</p>
            <a href="resources.html#insights" class="resource-link">View Insights →</a>
        </div>
        
        <div class="resource-card">
            <i class="fas fa-download"></i>
            <h3>Free Templates</h3>
            <p>Project templates, code snippets, and starter kits</p>
            <a href="resources.html#templates" class="resource-link">Download Now →</a>
        </div>
    </div>
</section>
```

### 6. Portfolio Showcase (NEW)

**Research & Include:**
- **Case Studies**: Detailed project breakdowns with challenges and solutions
- **Technology Stack**: Tools and frameworks used for each project
- **Results Metrics**: Performance improvements, cost savings, user engagement
- **Client Testimonials**: Success stories and feedback
- **Project Categories**: Web development, ML models, data analysis, consulting

### 7. AI Development Blog/Insights (NEW)

**Research Topics to Cover:**
- **"Getting Started with AI Development in 2025"**
- **"Top 10 AI Tools Every Developer Should Know"**
- **"How to Price AI Development Projects"**
- **"Building Your First Machine Learning Model"**
- **"AI Ethics: What Every Developer Must Consider"**
- **"From Idea to Deployment: AI Project Lifecycle"**

### 8. Interactive AI Tools Section (NEW)

**Research & Implement:**
- **AI Project Cost Calculator**: Interactive tool to estimate project costs
- **Skill Assessment Quiz**: Help visitors identify their AI readiness
- **Technology Recommendation Engine**: Suggest tools based on project needs
- **ROI Calculator**: Show potential returns on AI investments
- **Learning Path Generator**: Personalized AI learning roadmap

## Advanced Features to Research & Implement

### 1. AI-Powered Site Features
- **Intelligent chatbot** for customer service
- **Personalized content** based on visitor behavior
- **Smart contact forms** with automated routing
- **Dynamic pricing** based on project complexity

### 2. Industry Data Integration
- **Live job market data** for AI positions
- **Real-time technology trends** and adoption rates
- **Salary benchmarking** tools
- **Skill demand analytics**

### 3. Community Features
- **Client success stories** with measurable outcomes
- **Industry expert interviews** and insights
- **Monthly AI trends** newsletter
- **Webinar series** on AI development topics

## CSS Architecture

### Color System
```css
:root {
    --primary-color: #FF1493;      /* Hot Pink */
    --secondary-color: #FF69B4;    /* Medium Pink */
    --accent-color: #FFB6C1;       /* Light Pink */
    --dark-bg: #1a1a2e;           /* Dark Background */
    --darker-bg: #16213e;         /* Darker Sections */
    --text-light: #ffffff;
    --text-gray: #cccccc;
    --success-color: #00ff88;
    --warning-color: #ffaa00;
    --gradient-primary: linear-gradient(135deg, #FF1493, #FF69B4);
    --gradient-success: linear-gradient(135deg, #00ff88, #00cc6a);
}
```

### Component System
```css
/* Service cards with pricing */
.service-card {
    background: var(--darker-bg);
    border: 1px solid rgba(255, 20, 147, 0.2);
    border-radius: 16px;
    padding: 2rem;
    transition: all 0.3s ease;
    position: relative;
    overflow: hidden;
}

.service-card.featured {
    border-color: var(--primary-color);
    transform: scale(1.05);
}

.service-card:hover {
    transform: translateY(-8px);
    border-color: var(--primary-color);
    box-shadow: 0 20px 40px rgba(255, 20, 147, 0.3);
}

.pricing {
    font-size: 2rem;
    font-weight: 700;
    color: var(--primary-color);
    margin: 1rem 0;
}

.service-features {
    list-style: none;
    padding: 0;
    margin: 1.5rem 0;
}

.service-features li {
    padding: 0.5rem 0;
    color: var(--text-gray);
    position: relative;
    padding-left: 1.5rem;
}

.service-features li::before {
    content: '✓';
    position: absolute;
    left: 0;
    color: var(--success-color);
    font-weight: bold;
}
```

## JavaScript Functionality

### Interactive Pricing Calculator
```javascript
// AI Project Cost Calculator
class ProjectCalculator {
    constructor() {
        this.baseRates = {
            'ml-model': 5000,
            'web-app': 2500,
            'data-analysis': 3000,
            'consulting': 1500
        };
        this.complexityMultipliers = {
            'simple': 1,
            'moderate': 1.5,
            'complex': 2.5
        };
    }
    
    calculatePrice(projectType, complexity, timeline) {
        let basePrice = this.baseRates[projectType];
        let complexityMultiplier = this.complexityMultipliers[complexity];
        let rushMultiplier = timeline < 30 ? 1.5 : 1;
        
        return Math.round(basePrice * complexityMultiplier * rushMultiplier);
    }
}

// Initialize calculator
const calculator = new ProjectCalculator();

// Update price display in real-time
function updatePricing() {
    const projectType = document.querySelector('#project-type').value;
    const complexity = document.querySelector('#complexity').value;
    const timeline = document.querySelector('#timeline').value;
    
    const estimatedPrice = calculator.calculatePrice(projectType, complexity, timeline);
    document.querySelector('#price-estimate').textContent = `$${estimatedPrice.toLocaleString()}`;
}
```

### Skill Assessment Tool
```javascript
// AI Readiness Assessment
const assessmentQuestions = [
    {
        question: "What's your programming experience level?",
        options: ["Beginner", "Intermediate", "Advanced", "Expert"],
        weights: [1, 2, 3, 4]
    },
    {
        question: "Have you worked with data analysis tools?",
        options: ["Never", "Basic Excel", "Python/R", "Advanced Analytics"],
        weights: [1, 2, 3, 4]
    },
    // Add more questions...
];

function generateLearningPath(score) {
    if (score < 10) {
        return "Foundation Track: Start with Python basics and data fundamentals";
    } else if (score < 20) {
        return "Intermediate Track: Focus on machine learning libraries and projects";
    } else {
        return "Advanced Track: Deep learning, MLOps, and specialized applications";
    }
}
```

## Research Areas for Content Creation

### 1. Market Research
- **Current AI development costs** in the industry
- **Most in-demand AI skills** and technologies
- **Success metrics** for AI projects
- **Common challenges** in AI implementation
- **ROI data** for different types of AI projects

### 2. Technical Research
- **Latest AI frameworks** and their use cases
- **Best practices** for AI project management
- **Deployment strategies** for AI applications
- **Performance optimization** techniques
- **Security considerations** for AI systems

### 3. Educational Content Research
- **Learning pathways** for different AI careers
- **Certification programs** and their value
- **Open source projects** for skill building
- **Industry mentorship** opportunities
- **Networking events** and communities

### 4. Business Intelligence
- **Pricing strategies** for AI services
- **Client acquisition** methods
- **Project scoping** best practices
- **Contract templates** and legal considerations
- **Quality assurance** processes

## Success Metrics & Analytics

### Conversion Tracking
- **Contact form submissions** by service type
- **Resource downloads** and engagement
- **Webinar signups** and attendance
- **Portfolio consultation** requests
- **Blog engagement** and time on page

### User Journey Analysis
- **Most visited** service pages
- **Drop-off points** in the conversion funnel
- **Mobile vs desktop** usage patterns
- **Geographic distribution** of visitors
- **Referral sources** and campaign effectiveness

## Implementation Phases

### Phase 1: Foundation & Research (Week 1-2)
1. **Market research** on AI development services and pricing
2. **Competitor analysis** of similar service providers
3. **Content research** for all educational and resource sections
4. **Technical research** on current AI tools and frameworks
5. **Set up basic HTML structure** with responsive design
6. **Implement core CSS** with pink theme and animations

### Phase 2: Core Services & Content (Week 3-4)
1. **Develop service pages** with detailed descriptions and pricing
2. **Create resources section** with comprehensive AI information
3. **Build portfolio showcase** with case studies
4. **Implement coaching services** section with booking integration
5. **Add interactive elements** like calculators and assessments

### Phase 3: Advanced Features & Polish (Week 5-6)
1. **Integrate AI-powered features** (chatbot, personalization)
2. **Add blog section** with researched content
3. **Implement analytics** and conversion tracking
4. **Optimize for performance** and SEO
5. **Final testing** across all devices and browsers
6. **Deploy to production** with monitoring setup

This comprehensive prompt ensures the AI will create not just a beautiful website, but a valuable resource hub that positions Tiffany as the go-to expert for AI development services while providing genuine value to potential clients through research-backed content and tools.

## Complete vercel.json Security Configuration

```json
{
  "cleanUrls": true,
  "trailingSlash": false,
  "rewrites": [
    {
      "source": "/ai-development",
      "destination": "/ai-development.html"
    },
    {
      "source": "/coaching",
      "destination": "/coaching.html"
    },
    {
      "source": "/about",
      "destination": "/about.html"
    },
    {
      "source": "/portfolio",
      "destination": "/portfolio.html"
    },
    {
      "source": "/resources",
      "destination": "/resources.html"
    },
    {
      "source": "/blog",
      "destination": "/blog.html"
    },
    {
      "source": "/speaking",
      "destination": "/speaking.html"
    },
    {
      "source": "/webinar",
      "destination": "/webinar.html"
    }
  ],
  "redirects": [
    {
      "source": "/ai-development.html",
      "destination": "/ai-development",
      "permanent": true
    },
    {
      "source": "/coaching.html",
      "destination": "/coaching",
      "permanent": true
    },
    {
      "source": "/about.html",
      "destination": "/about",
      "permanent": true
    },
    {
      "source": "/portfolio.html",
      "destination": "/portfolio",
      "permanent": true
    },
    {
      "source": "/resources.html",
      "destination": "/resources",
      "permanent": true
    },
    {
      "source": "/blog.html",
      "destination": "/blog",
      "permanent": true
    },
    {
      "source": "/speaking.html",
      "destination": "/speaking",
      "permanent": true
    },
    {
      "source": "/webinar.html",
      "destination": "/webinar",
      "permanent": true
    }
  ],
  "headers": [
    {
      "source": "/(.*)",
      "headers": [
        {
          "key": "Cache-Control",
          "value": "public, max-age=0, must-revalidate"
        },
        {
          "key": "Strict-Transport-Security",
          "value": "max-age=31536000; includeSubDomains; preload"
        },
        {
          "key": "X-Content-Type-Options",
          "value": "nosniff"
        },
        {
          "key": "X-Frame-Options",
          "value": "DENY"
        },
        {
          "key": "X-XSS-Protection",
          "value": "1; mode=block"
        },
        {
          "key": "Referrer-Policy",
          "value": "strict-origin-when-cross-origin"
        },
        {
          "key": "Content-Security-Policy",
          "value": "default-src 'self'; script-src 'self' 'unsafe-inline' cdnjs.cloudflare.com; style-src 'self' 'unsafe-inline' fonts.googleapis.com cdnjs.cloudflare.com; font-src 'self' fonts.gstatic.com; img-src 'self' data:; connect-src 'self'"
        }
      ]
    }
  ]
}
```

## Security Implementation Checklist

### ✅ HTTPS Enforcement
- [ ] All pages served over HTTPS
- [ ] HTTP requests automatically redirect to HTTPS
- [ ] HSTS header prevents downgrade attacks

### ✅ Security Headers
- [ ] Strict-Transport-Security implemented
- [ ] X-Content-Type-Options: nosniff
- [ ] X-Frame-Options: DENY (prevents clickjacking)
- [ ] X-XSS-Protection: 1; mode=block
- [ ] Referrer-Policy: strict-origin-when-cross-origin
- [ ] Content-Security-Policy configured

### ✅ HTML Security
- [ ] All HTML files include security meta tags
- [ ] Content-Security-Policy meta tag for upgrade-insecure-requests
- [ ] Referrer meta tag properly configured

### ✅ Content Security Policy
- [ ] Script sources limited to self and trusted CDNs
- [ ] Style sources limited to self and Google Fonts
- [ ] Font sources limited to self and Google Fonts
- [ ] Image sources limited to self and data URIs
- [ ] Connect sources limited to self

### ✅ Performance & Caching
- [ ] Cache-Control headers configured
- [ ] Clean URLs enabled
- [ ] Trailing slash handling configured
- [ ] Proper redirects for SEO

This security configuration ensures the Data Sistah website is protected against common web vulnerabilities while maintaining excellent performance and user experience.
