# Title
Implement the Core AI Narrative Generation Logic

# Introduction
This is the "brain" of the application. Create the service that orchestrates the entire AI process, from analyzing user input to generating personalized sales content. This module combines the PDF data, knowledge base, and user context to create compelling sales narratives.

# Tasks
- [ ] Implement the "Four-Layer Analysis Framework" logic: take user's natural language input, and through an LLM call, classify it into Objective Tags, Archetype, Pain Points, and Solution Needs
- [ ] Implement the "Instruction Set" logic: based on the output of the analysis, query the knowledge base (004) to retrieve the correct FAB-P script
- [ ] Implement the final content generation step: send the retrieved script, the parsed PDF data (003), and the user's context to the LLM to generate the final, personalized text content for each PPT slide
- [ ] Create prompt engineering templates for consistent AI responses
- [ ] Implement content validation to ensure generated text meets quality standards
- [ ] Add fallback mechanisms for when AI analysis fails or produces low-quality content
- [ ] Implement content caching to improve response times for similar requests
- [ ] Create AI performance monitoring and analytics
- [ ] Write comprehensive tests for AI logic accuracy and consistency
- [ ] Implement rate limiting and cost management for LLM API calls

# Dependencies
- [ ] 003-feat-pdf-parser (for structured PDF data)
- [ ] 004-feat-knowledge-base-setup (for FAB-P scripts)
- [ ] {DEP-002} LLM API integration

# Status History
- 2025-01-27: Created 