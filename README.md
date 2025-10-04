import React, { useState } from 'react';
import { Zap, Check, Calendar, MessageCircle, TrendingUp, Clock, Users, BarChart3, Bot, Sparkles, ChevronRight, Play, Star, Shield, Globe, Moon, Sun, Menu, X } from 'lucide-react';

export default function AIAgentWebsite() {
  const [darkMode, setDarkMode] = useState(false);
  const [mobileMenuOpen, setMobileMenuOpen] = useState(false);
  const [showDemo, setShowDemo] = useState(false);

  const capabilities = [
    {
      icon: MessageCircle,
      title: 'Instant Replies',
      automation: 'Responds to new inquiries via WhatsApp, Email, or Web Chat',
      outcome: 'Never miss a customer again'
    },
    {
      icon: Users,
      title: 'Smart Qualification',
      automation: 'Identifies serious leads based on intent and data',
      outcome: 'Focus only on high-value opportunities'
    },
    {
      icon: Calendar,
      title: 'Appointment Booking',
      automation: 'Integrates with your calendar to schedule meetings',
      outcome: 'No back-and-forth with clients'
    },
    {
      icon: Clock,
      title: 'Automated Follow-Ups',
      automation: 'Sends reminders and re-engagement messages',
      outcome: 'Converts cold leads automatically'
    },
    {
      icon: TrendingUp,
      title: 'System Updates',
      automation: 'Logs every chat and lead into your CRM or database',
      outcome: 'Keeps your data clean & organized'
    },
    {
      icon: BarChart3,
      title: 'Daily/Weekly Reports',
      automation: 'Summarizes your performance automatically',
      outcome: 'Stay updated without manual tracking'
    }
  ];

  const steps = [
    { num: '1', text: 'Capture new inquiries' },
    { num: '2', text: 'AI processes and qualifies them' },
    { num: '3', text: 'Personalized response sent instantly' },
    { num: '4', text: 'Schedule meetings or tasks automatically' },
    { num: '5', text: 'Follow-ups handled on autopilot' },
    { num: '6', text: 'Get daily summaries and insights' }
  ];

  const testimonials = [
    { text: "It feels like having a full-time employee that never sleeps.", author: "Sarah Chen", role: "CEO, TechStart" },
    { text: "We save 5+ hours daily and never miss a lead anymore.", author: "Mike Rodriguez", role: "Sales Director" },
    { text: "Automation that actually feels human.", author: "Emma Wilson", role: "Marketing Head" }
  ];

  const benefits = [
    '4–6 hours saved daily',
    '3x faster customer response time',
    '30–40% more qualified leads',
    'Zero missed opportunities'
  ];

  const integrations = [
    { category: 'Calendars', items: ['Google Calendar', 'Outlook', 'Calendly'] },
    { category: 'Communication', items: ['WhatsApp', 'Slack', 'Email'] },
    { category: 'CRMs', items: ['HubSpot', 'Notion', 'Airtable'] },
    { category: 'Ads & Forms', items: ['Meta Ads', 'Google Ads', 'Typeform'] }
  ];

  const pricing = [
    {
      name: 'Starter',
      price: '$49',
      features: ['AI responses', 'Lead qualification', 'Email support', 'Basic analytics', '100 conversations/month'],
      popular: false
    },
    {
      name: 'Pro',
      price: '$99',
      features: ['Everything in Starter', 'Scheduling automation', 'Automated follow-ups', 'Priority support', '500 conversations/month', 'Custom workflows'],
      popular: true
    },
    {
      name: 'Premium',
      price: '$199',
      features: ['Everything in Pro', 'CRM sync', 'Advanced reports', 'API access', 'Unlimited conversations', 'Dedicated account manager', 'Custom AI training'],
      popular: false
    }
  ];

  const whyUs = [
    { icon: Bot, title: 'Custom Automation Workflows', desc: 'Built exactly for your business processes' },
    { icon: Sparkles, title: 'Powered by Advanced AI', desc: 'Uses the latest language models for natural conversation' },
    { icon: MessageCircle, title: 'Omni-Channel Messaging', desc: 'Works across Email, WhatsApp, SMS, and Chat' },
    { icon: Zap, title: 'Fast Deployment', desc: 'Setup in under 48 hours' },
    { icon: Users, title: 'Dedicated Support', desc: 'Real humans to help you every step of the way' }
  ];

  const Navigation = () => (
    <nav className={`${darkMode ? 'bg-gray-900/95 backdrop-blur-lg border-gray-800' : 'bg-white/95 backdrop-blur-lg'} shadow-sm sticky top-0 z-50 border-b transition-colors`}>
      <div className="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div className="flex justify-between items-center h-16">
          <div className="flex items-center space-x-2">
            <div className={`w-10 h-10 rounded-xl ${darkMode ? 'bg-gradient-to-br from-blue-500 to-purple-600' : 'bg-gradient-to-br from-blue-600 to-purple-700'} flex items-center justify-center`}>
              <Bot className="w-6 h-6 text-white" />
            </div>
            <span className={`text-xl font-bold ${darkMode ? 'text-white' : 'text-gray-900'}`}>AI Assistant Pro</span>
          </div>

          <div className="hidden md:flex items-center space-x-8">
            <a href="#features" className={`${darkMode ? 'text-gray-300 hover:text-blue-400' : 'text-gray-700 hover:text-blue-600'} transition`}>Features</a>
            <a href="#how-it-works" className={`${darkMode ? 'text-gray-300 hover:text-blue-400' : 'text-gray-700 hover:text-blue-600'} transition`}>How It Works</a>
            <a href="#pricing" className={`${darkMode ? 'text-gray-300 hover:text-blue-400' : 'text-gray-700 hover:text-blue-600'} transition`}>Pricing</a>
            <button 
              onClick={() => setDarkMode(!darkMode)} 
              className={`p-2 rounded-lg ${darkMode ? 'bg-gray-800 text-yellow-400' : 'bg-gray-100 text-gray-700'} hover:scale-110 transition-transform`}
            >
              {darkMode ? <Sun className="w-5 h-5" /> : <Moon className="w-5 h-5" />}
            </button>
            <button className={`${darkMode ? 'bg-gradient-to-r from-blue-500 to-purple-600 hover:from-blue-600 hover:to-purple-700' : 'bg-gradient-to-r from-blue-600 to-purple-700 hover:from-blue-700 hover:to-purple-800'} text-white px-6 py-2.5 rounded-lg font-semibold transition shadow-lg`}>
              Book a Demo
            </button>
          </div>

          <button className="md:hidden" onClick={() => setMobileMenuOpen(!mobileMenuOpen)}>
            {mobileMenuOpen ? <X className={`w-6 h-6 ${darkMode ? 'text-white' : 'text-gray-900'}`} /> : <Menu className={`w-6 h-6 ${darkMode ? 'text-white' : 'text-gray-900'}`} />}
          </button>
        </div>

        {mobileMenuOpen && (
          <div className="md:hidden pb-4 space-y-2">
            <a href="#features" className={`block py-2 ${darkMode ? 'text-gray-300' : 'text-gray-700'}`}>Features</a>
            <a href="#how-it-works" className={`block py-2 ${darkMode ? 'text-gray-300' : 'text-gray-700'}`}>How It Works</a>
            <a href="#pricing" className={`block py-2 ${darkMode ? 'text-gray-300' : 'text-gray-700'}`}>Pricing</a>
            <button onClick={() => setDarkMode(!darkMode)} className={`flex items-center w-full py-2 ${darkMode ? 'text-gray-300' : 'text-gray-700'}`}>
              {darkMode ? <Sun className="w-4 h-4 mr-2" /> : <Moon className="w-4 h-4 mr-2" />}
              {darkMode ? 'Light Mode' : 'Dark Mode'}
            </button>
          </div>
        )}
      </div>
    </nav>
  );

  return (
    <div className={`${darkMode ? 'bg-gray-900' : 'bg-white'} transition-colors`}>
      <Navigation />

      {/* Hero Section */}
      <section className={`${darkMode ? 'bg-gradient-to-br from-gray-900 via-blue-900/20 to-purple-900/20' : 'bg-gradient-to-br from-blue-50 via-purple-50 to-pink-50'} py-20 md:py-32`}>
        <div className="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
          <div className="grid md:grid-cols-2 gap-12 items-center">
            <div>
              <div className={`inline-flex items-center space-x-2 ${darkMode ? 'bg-blue-900/30 border-blue-700' : 'bg-blue-100 border-blue-200'} border px-4 py-2 rounded-full mb-6`}>
                <Sparkles className={`w-4 h-4 ${darkMode ? 'text-blue-400' : 'text-blue-600'}`} />
                <span className={`text-sm font-medium ${darkMode ? 'text-blue-400' : 'text-blue-600'}`}>AI-Powered Automation</span>
              </div>
              <h1 className={`text-5xl md:text-6xl font-bold ${darkMode ? 'text-white' : 'text-gray-900'} mb-6 leading-tight`}>
                Your 24/7 AI Assistant
                <span className={`block ${darkMode ? 'bg-gradient-to-r from-blue-400 to-purple-500' : 'bg-gradient-to-r from-blue-600 to-purple-600'} bg-clip-text text-transparent`}>
                  Automate Everything
                </span>
              </h1>
              <p className={`text-xl ${darkMode ? 'text-gray-300' : 'text-gray-600'} mb-8 leading-relaxed`}>
                Stop wasting hours on repetitive tasks. Our AI Agent responds to customers, qualifies leads, books appointments, and sends reports — automatically.
              </p>
              <div className="flex flex-col sm:flex-row gap-4">
                <button className={`${darkMode ? 'bg-gradient-to-r from-blue-500 to-purple-600 hover:from-blue-600 hover:to-purple-700' : 'bg-gradient-to-r from-blue-600 to-purple-700 hover:from-blue-700 hover:to-purple-800'} text-white px-8 py-4 rounded-xl font-semibold transition shadow-xl flex items-center justify-center space-x-2`}>
                  <span>Book a Demo</span>
                  <ChevronRight className="w-5 h-5" />
                </button>
                <button className={`${darkMode ? 'bg-gray-800 border-gray-700 text-white hover:bg-gray-700' : 'bg-white border-gray-300 text-gray-900 hover:bg-gray-50'} border-2 px-8 py-4 rounded-xl font-semibold transition shadow-lg`}>
                  Try Free for 7 Days
                </button>
              </div>
              <p className={`mt-4 text-sm ${darkMode ? 'text-gray-400' : 'text-gray-500'}`}>✓ No credit card required • ✓ Setup in 48 hours</p>
            </div>
            <div className={`${darkMode ? 'bg-gradient-to-br from-gray-800 to-gray-900 border-gray-700' : 'bg-gradient-to-br from-white to-blue-50 border-blue-200'} border-2 rounded-2xl p-8 shadow-2xl`}>
              <div className="space-y-4">
                <div className={`flex items-center space-x-3 ${darkMode ? 'bg-gray-700/50' : 'bg-white'} p-4 rounded-lg shadow`}>
                  <Bot className={`w-8 h-8 ${darkMode ? 'text-blue-400' : 'text-blue-600'}`} />
                  <div>
                    <p className={`font-semibold ${darkMode ? 'text-white' : 'text-gray-900'}`}>AI responding to chat...</p>
                    <p className={`text-sm ${darkMode ? 'text-gray-400' : 'text-gray-500'}`}>Qualifying lead automatically</p>
                  </div>
                </div>
                <div className={`flex items-center space-x-3 ${darkMode ? 'bg-gray-700/50' : 'bg-white'} p-4 rounded-lg shadow`}>
                  <Calendar className={`w-8 h-8 ${darkMode ? 'text-purple-400' : 'text-purple-600'}`} />
                  <div>
                    <p className={`font-semibold ${darkMode ? 'text-white' : 'text-gray-900'}`}>Meeting scheduled</p>
                    <p className={`text-sm ${darkMode ? 'text-gray-400' : 'text-gray-500'}`}>Calendar invite sent</p>
                  </div>
                </div>
                <div className={`flex items-center space-x-3 ${darkMode ? 'bg-gray-700/50' : 'bg-white'} p-4 rounded-lg shadow`}>
                  <BarChart3 className={`w-8 h-8 ${darkMode ? 'text-green-400' : 'text-green-600'}`} />
                  <div>
                    <p className={`font-semibold ${darkMode ? 'text-white' : 'text-gray-900'}`}>Daily report generated</p>
                    <p className={`text-sm ${darkMode ? 'text-gray-400' : 'text-gray-500'}`}>15 new leads today</p>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </section>

      {/* What AI Can Do Section */}
      <section id="features" className={`py-20 ${darkMode ? 'bg-gray-900' : 'bg-white'}`}>
        <div className="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
          <div className="text-center mb-16">
            <h2 className={`text-4xl md:text-5xl font-bold ${darkMode ? 'text-white' : 'text-gray-900'} mb-4`}>
              What Our AI Agent Can Do for You
            </h2>
            <p className={`text-xl ${darkMode ? 'text-gray-400' : 'text-gray-600'}`}>
              From first contact to follow-up — automation that works while you sleep
            </p>
          </div>

          <div className="grid md:grid-cols-2 lg:grid-cols-3 gap-6">
            {capabilities.map((cap, idx) => {
              const Icon = cap.icon;
              return (
                <div key={idx} className={`${darkMode ? 'bg-gray-800 border-gray-700 hover:border-blue-500' : 'bg-gradient-to-br from-white to-blue-50 border-blue-100 hover:border-blue-300'} border-2 rounded-xl p-6 transition-all duration-300 hover:shadow-xl`}>
                  <div className={`w-12 h-12 ${darkMode ? 'bg-blue-900/50' : 'bg-blue-100'} rounded-lg flex items-center justify-center mb-4`}>
                    <Icon className={`w-6 h-6 ${darkMode ? 'text-blue-400' : 'text-blue-600'}`} />
                  </div>
                  <h3 className={`text-xl font-bold ${darkMode ? 'text-white' : 'text-gray-900'} mb-2`}>{cap.title}</h3>
                  <p className={`${darkMode ? 'text-gray-400' : 'text-gray-600'} text-sm mb-3`}>{cap.automation}</p>
                  <div className={`${darkMode ? 'bg-green-900/30 border-green-700' : 'bg-green-50 border-green-200'} border rounded-lg px-3 py-2`}>
                    <p className={`text-sm font-semibold ${darkMode ? 'text-green-400' : 'text-green-700'}`}>✓ {cap.outcome}</p>
                  </div>
                </div>
              );
            })}
          </div>
        </div>
      </section>

      {/* How It Works Section */}
      <section id="how-it-works" className={`py-20 ${darkMode ? 'bg-gray-800' : 'bg-gray-50'}`}>
        <div className="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
          <div className="text-center mb-16">
            <h2 className={`text-4xl md:text-5xl font-bold ${darkMode ? 'text-white' : 'text-gray-900'} mb-4`}>
              How It Works
            </h2>
            <p className={`text-xl ${darkMode ? 'text-gray-400' : 'text-gray-600'}`}>
              From first contact to follow-up — your AI agent manages it all
            </p>
          </div>

          <div className="grid md:grid-cols-3 gap-8">
            {steps.map((step, idx) => (
              <div key={idx} className="relative">
                <div className={`${darkMode ? 'bg-gray-900 border-gray-700' : 'bg-white border-gray-200'} border-2 rounded-xl p-6 h-full`}>
                  <div className={`w-12 h-12 rounded-full ${darkMode ? 'bg-gradient-to-br from-blue-500 to-purple-600' : 'bg-gradient-to-br from-blue-600 to-purple-700'} flex items-center justify-center text-white font-bold text-xl mb-4`}>
                    {step.num}
                  </div>
                  <p className={`text-lg ${darkMode ? 'text-white' : 'text-gray-900'} font-semibold`}>{step.text}</p>
                </div>
                {idx < steps.length - 3 && (
                  <ChevronRight className={`hidden md:block absolute top-1/2 -right-4 w-8 h-8 ${darkMode ? 'text-blue-400' : 'text-blue-600'} transform -translate-y-1/2`} />
                )}
              </div>
            ))}
          </div>
        </div>
      </section>

      {/* Testimonials Section */}
      <section className={`py-20 ${darkMode ? 'bg-gray-900' : 'bg-white'}`}>
        <div className="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
          <div className="text-center mb-16">
            <h2 className={`text-4xl md:text-5xl font-bold ${darkMode ? 'text-white' : 'text-gray-900'} mb-4`}>
              Why Businesses Love It
            </h2>
          </div>

          <div className="grid md:grid-cols-3 gap-8">
            {testimonials.map((test, idx) => (
              <div key={idx} className={`${darkMode ? 'bg-gray-800 border-gray-700' : 'bg-gradient-to-br from-white to-purple-50 border-purple-100'} border-2 rounded-xl p-8`}>
                <div className="flex mb-4">
                  {[...Array(5)].map((_, i) => (
                    <Star key={i} className="w-5 h-5 fill-yellow-400 text-yellow-400" />
                  ))}
                </div>
                <p className={`text-lg ${darkMode ? 'text-gray-300' : 'text-gray-700'} mb-6 italic`}>"{test.text}"</p>
                <div>
                  <p className={`font-semibold ${darkMode ? 'text-white' : 'text-gray-900'}`}>{test.author}</p>
                  <p className={`text-sm ${darkMode ? 'text-gray-400' : 'text-gray-600'}`}>{test.role}</p>
                </div>
              </div>
            ))}
          </div>
        </div>
      </section>

      {/* Benefits Section */}
      <section className={`py-20 ${darkMode ? 'bg-gradient-to-br from-blue-900/20 to-purple-900/20' : 'bg-gradient-to-br from-blue-600 to-purple-700'}`}>
        <div className="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
          <div className="text-center mb-12">
            <h2 className="text-4xl md:text-5xl font-bold text-white mb-4">
              What You'll Gain
            </h2>
          </div>
          <div className="grid md:grid-cols-2 lg:grid-cols-4 gap-6">
            {benefits.map((benefit, idx) => (
              <div key={idx} className={`${darkMode ? 'bg-gray-800/50 border-gray-700' : 'bg-white/10 border-white/20'} backdrop-blur-lg border rounded-xl p-6 text-center`}>
                <Check className="w-12 h-12 text-green-400 mx-auto mb-3" />
                <p className="text-xl font-bold text-white">{benefit}</p>
              </div>
            ))}
          </div>
        </div>
      </section>

      {/* Integrations Section */}
      <section className={`py-20 ${darkMode ? 'bg-gray-900' : 'bg-white'}`}>
        <div className="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
          <div className="text-center mb-16">
            <h2 className={`text-4xl md:text-5xl font-bold ${darkMode ? 'text-white' : 'text-gray-900'} mb-4`}>
              Integrates Seamlessly
            </h2>
            <p className={`text-xl ${darkMode ? 'text-gray-400' : 'text-gray-600'}`}>
              Compatible with your favorite tools — no code needed
            </p>
          </div>

          <div className="grid md:grid-cols-2 lg:grid-cols-4 gap-6">
            {integrations.map((int, idx) => (
              <div key={idx} className={`${darkMode ? 'bg-gray-800 border-gray-700' : 'bg-gray-50 border-gray-200'} border rounded-xl p-6`}>
                <Globe className={`w-8 h-8 ${darkMode ? 'text-blue-400' : 'text-blue-600'} mb-4`} />
                <h3 className={`font-bold ${darkMode ? 'text-white' : 'text-gray-900'} mb-3`}>{int.category}</h3>
                <ul className="space-y-2">
                  {int.items.map((item, i) => (
                    <li key={i} className={`text-sm ${darkMode ? 'text-gray-400' : 'text-gray-600'}`}>• {item}</li>
                  ))}
                </ul>
              </div>
            ))}
          </div>
        </div>
      </section>

      {/* Pricing Section */}
      <section id="pricing" className={`py-20 ${darkMode ? 'bg-gray-800' : 'bg-gray-50'}`}>
        <div className="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
          <div className="text-center mb-16">
            <h2 className={`text-4xl md:text-5xl font-bold ${darkMode ? 'text-white' : 'text-gray-900'} mb-4`}>
              Simple & Transparent Pricing
            </h2>
            <p className={`text-xl ${darkMode ? 'text-gray-400' : 'text-gray-600'}`}>
              Start free, scale as you grow
            </p>
          </div>

          <div className="grid md:grid-cols-3 gap-8">
            {pricing.map((plan, idx) => (
              <div key={idx} className={`${darkMode ? 'bg-g