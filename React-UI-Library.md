# React UI Library Agent Specification

## Project Overview
Create a comprehensive, responsive React UI component library with Storybook documentation that works seamlessly across all devices and screen sizes.

## Core Requirements

### 🚨 **HIGHEST PRIORITY: Storybook Documentation**
**Storybook implementation and documentation is the PRIMARY requirement and must be completed FIRST before any component development begins. Every component listed below MUST have comprehensive Storybook documentation as specified in section 5.**

### 1. Project Setup & Architecture
- Initialize a React TypeScript project with modern tooling
- Set up build system using Rollup/Vite for optimal bundle size
- Configure ESLint, Prettier, and Husky for code quality
- Implement semantic versioning and automated releases
- Create proper package.json with peer dependencies for React
- Set up CI/CD pipeline for automated testing and publishing

### 2. Design System Foundation
- Implement a comprehensive design token system for colors, typography, spacing, and breakpoints
- Create a mobile-first responsive approach with breakpoint utilities
- Establish consistent naming conventions following BEM or similar methodology
- Design a scalable CSS-in-JS solution (Styled Components/Emotion) or CSS Modules
- **Multi-Theme Architecture**: Implement a robust theming system supporting:
  
  #### Default Themes
  - **Light Theme**: Standard light mode with modern, clean aesthetics
  - **Dark Theme**: Professional dark mode with proper contrast ratios
  
  #### Additional Theme Variants
  - **Pure White Theme**: Minimal high-contrast theme with:
    - Pure white (#FFFFFF) backgrounds
    - Sharp black (#000000) text and borders
    - Minimal use of grays for subtle elements
    - Clean, sterile aesthetic for medical/professional apps
  
  - **True Black Theme**: High-contrast dark theme featuring:
    - Pure black (#000000) backgrounds for OLED displays
    - Bright white (#FFFFFF) text
    - Minimal color accents for better accessibility
    - Battery-optimized for mobile devices
  
  - **E-Commerce Dark Theme**: Sophisticated dark theme optimized for shopping experiences:
    - Rich dark navy (#0A0E1A) primary background
    - Charcoal gray (#1A1D26) secondary surfaces
    - Warm accent colors: Gold (#D4AF37) for premium elements
    - Electric blue (#00D4FF) for CTAs and interactive elements
    - Soft emerald (#50C878) for success states and prices
    - Muted orange (#FF6B35) for sale/discount indicators
    - Enhanced product imagery contrast
    - Optimized for product photography and visual hierarchy
    - Premium feel with subtle gradients and shadows
  
- **Theme System Features**:
  - Runtime theme switching with smooth transitions
  - CSS custom properties for efficient theme application
  - Theme-aware component variants
  - Automatic contrast adjustment for accessibility
  - Theme persistence in localStorage
  - System theme detection and auto-switching
- Create accessibility-first components following WCAG 2.1 AA standards across all themes
- Implement theme validation to ensure contrast ratios meet accessibility standards

### 3. Component Development Strategy

#### Phase 1: Foundational Components (Priority 1)
- **Grid/Layout System**: Responsive grid with Row, Col, Container, Section components
- **Typography**: H1-H6, Paragraph, Text, Caption, Blockquote, Code, Pre with responsive scaling
- **Button**: Primary, Secondary, Ghost, Icon, Link, Floating Action Button (FAB) variants with loading states
- **Input**: Text, Email, Password, Number, Search, URL, Tel with validation states and prefix/suffix
- **Spacing Utilities**: Spacer, Stack, Box, Divider, Separator for layout management
- **Icons**: SVG icon system with 500+ icons, customizable size, color, and animation states
- **Image**: Responsive image with lazy loading, placeholder, fallback, and zoom functionality
- **Link**: Internal, external, and anchor links with various styles and states

#### Phase 2: Form & Input Components (Priority 2)
- **Textarea**: Multi-line input with auto-resize, character count, and rich text options
- **Checkbox**: With indeterminate state, validation, and group management
- **Radio Button**: Group management, validation, and custom styling options
- **Select/Dropdown**: Single, multi-select with search, async loading, and custom options
- **Toggle/Switch**: Animated on/off states with labels and descriptions
- **Slider**: Range, single value, vertical/horizontal with custom marks and tooltips
- **Date Picker**: Single date, date range, time selection, and calendar with localization
- **File Upload**: Drag & drop, multiple files, progress indication, and preview
- **Search**: Advanced search with filters, autocomplete, and recent searches
- **Rating**: Star rating, thumbs up/down, and custom rating systems
- **Form**: Form wrapper with validation, submission states, and error handling
- **Field**: Form field wrapper with labels, help text, and error states
- **OTP Input**: One-time password input with auto-focus and paste support

#### Phase 3: Feedback & Communication (Priority 3)
- **Alert/Banner**: Success, Warning, Error, Info variants with dismiss and actions
- **Toast/Snackbar**: Auto-dismiss, persistent, with action buttons and positioning
- **Modal/Dialog**: Accessible overlays, confirmation dialogs, and drawer variants
- **Tooltip/Popover**: Hover, click, focus triggers with smart positioning and rich content
- **Spinner/Loader**: Various animations, skeleton screens, and progress indicators
- **Progress Bar**: Determinate, indeterminate, circular, and step progress
- **Empty State**: No data, error, loading states with illustrations and actions
- **Status Indicator**: Online/offline, connection status, and system health indicators
- **Notification**: System notifications, badges, and announcement bars

#### Phase 4: Data Display Components (Priority 4)
- **Card**: Flexible container with header, body, footer, media, and interactive variants
- **Table**: Responsive with sorting, filtering, pagination, row selection, and expandable rows
- **Data Grid**: Advanced table with virtual scrolling, cell editing, and export functionality
- **Badge/Chip**: Status indicators, removable tags, filter chips, and interactive variants
- **Avatar**: Image, initials, icon variants with fallbacks, groups, and status indicators
- **List**: Simple, complex items, virtual scrolling, drag & drop, and selection states
- **Timeline**: Vertical, horizontal timelines with events, milestones, and interactive elements
- **Stat Card**: KPI displays, metrics, trends with charts and comparisons
- **Price Display**: Currency formatting, discounts, comparison pricing
- **Calendar**: Month view, week view, event management, and scheduling
- **Tree View**: Hierarchical data with expand/collapse, selection, and drag & drop
- **Code Block**: Syntax highlighting, copy functionality, line numbers, and diff view

#### Phase 5: Navigation Components (Priority 5)
- **Navbar/Header**: Responsive navigation with mobile hamburger menu, search, and user actions
- **Tabs**: Horizontal, vertical, scrollable with keyboard navigation and lazy loading
- **Breadcrumbs**: Hierarchical navigation with custom separators and overflow handling
- **Pagination**: Number-based, prev/next, infinite scroll, and load more patterns
- **Accordion**: Single, multiple expansion, nested accordions with animations
- **Menu/Sidebar**: Collapsible navigation, nested items, icons, and responsive behavior
- **Stepper**: Linear, non-linear progress indication for multi-step processes
- **Bottom Navigation**: Mobile-first navigation with badges and labels
- **Floating Navigation**: Sticky navigation, back-to-top, and quick actions

#### Phase 6: Media & Rich Content (Priority 6)
- **Video Player**: Custom controls, playlists, chapters, quality selection, and subtitles
- **Audio Player**: Music player, podcast player with waveforms and controls
- **Image Gallery**: Lightbox, carousel, grid view with zoom and fullscreen
- **Carousel/Slider**: Image carousel, content slider with touch support and indicators
- **Lightbox**: Image, video lightbox with thumbnails and navigation
- **PDF Viewer**: Embedded PDF display with controls and download options
- **Map**: Interactive maps with markers, overlays, and location services
- **Rich Text Editor**: WYSIWYG editor with formatting, media insertion, and export
- **Markdown Renderer**: Markdown to HTML with syntax highlighting and custom components

#### Phase 7: E-Commerce Specific Components (Priority 7)
- **Product Card**: Enhanced imagery, quick actions, variants, and wishlist integration
- **Product Gallery**: Zoom, 360° view, video integration, and thumbnail navigation
- **Price Component**: Regular, sale, bulk pricing with currency and localization
- **Add to Cart**: Button with quantity selector, variant selection, and loading states
- **Shopping Cart**: Mini cart, full cart, quantity updates, and checkout flow
- **Wishlist**: Add/remove, sharing, and organization features
- **Product Comparison**: Side-by-side comparison with specs and features
- **Review System**: Star ratings, comments, helpful votes, and moderation
- **Coupon Input**: Discount codes with validation and application feedback
- **Checkout Steps**: Multi-step checkout with validation and progress indication
- **Order Summary**: Itemized breakdown, taxes, shipping, and totals
- **Payment Methods**: Credit card, digital wallet, and alternative payment options

#### Phase 8: Advanced Interactive Components (Priority 8)
- **Drag & Drop**: Sortable lists, kanban boards, file uploads, and reordering
- **Resizable Panels**: Split panes, adjustable layouts, and collapsible sections
- **Virtual Scroller**: Efficient rendering for large datasets with smooth scrolling
- **Infinite Scroll**: Lazy loading content with loading indicators and error handling
- **Tour Guide**: Onboarding tours, feature highlights, and interactive tutorials
- **Command Palette**: Quick actions, search, and keyboard shortcuts
- **Context Menu**: Right-click menus with nested items and keyboard navigation
- **Mention**: @mentions with autocomplete and user search
- **Emoji Picker**: Emoji selection with categories, search, and recent usage
- **Color Picker**: HSL, RGB, hex color selection with presets and eyedropper

#### Phase 9: Data Visualization Components (Priority 9)
- **Charts**: Line, bar, pie, area charts with interactive legends and tooltips
- **Sparklines**: Inline mini charts for trends and quick data visualization
- **Heatmap**: Data density visualization with hover interactions
- **Gauge**: Progress gauges, speedometers, and circular progress indicators
- **Candlestick Chart**: Financial data visualization for trading applications
- **Gantt Chart**: Project timeline visualization with dependencies
- **Organizational Chart**: Hierarchy visualization with interactive nodes
- **Network Graph**: Node-link diagrams for relationship visualization

#### Phase 10: Specialized Components (Priority 10)
- **Chat Interface**: Message bubbles, typing indicators, file sharing, and emoji reactions
- **Comment System**: Threaded comments, replies, voting, and moderation
- **Activity Feed**: Social media style updates with actions and timestamps
- **Notification Center**: Grouped notifications with read/unread states and actions
- **Live Chat**: Real-time messaging with presence indicators and file sharing
- **Video Call**: WebRTC integration with controls and participant management
- **Drawing Canvas**: Freehand drawing, shapes, text annotations, and export
- **Signature Pad**: Digital signature capture with validation
- **QR Code**: QR code generation and scanning functionality
- **Barcode Scanner**: Camera integration for barcode reading
- **Geolocation**: Location services with maps and address autocomplete
- **Camera Capture**: Photo/video capture with preview and filters

### 4. Technical Specifications

#### Responsiveness Requirements
- Mobile-first CSS approach starting from 320px
- Breakpoints: xs (320px), sm (576px), md (768px), lg (992px), xl (1200px), xxl (1400px)
- Fluid typography using clamp() for smooth scaling
- Touch-friendly interaction targets (minimum 44px)
- Flexible layouts using CSS Grid and Flexbox

#### Accessibility Standards
- ARIA labels and roles for all interactive components
- Keyboard navigation support with visible focus indicators
- Screen reader compatibility with proper announcements
- Color contrast ratios meeting WCAG AA standards
- Reduced motion support for animations
- High contrast mode compatibility

#### Performance Optimization
- Tree-shaking support for individual component imports
- Lazy loading for heavy components
- Optimized bundle sizes with code splitting
- Minimal runtime dependencies
- Performance budgets and monitoring

### 5. Storybook Documentation Setup
- Configure Storybook 7+ with TypeScript support
- **Mandatory Component Documentation**: Every UI component MUST have corresponding Storybook documentation including:
  - Default story showcasing basic usage
  - All component variants and states (loading, error, disabled, etc.)
  - Interactive controls (knobs) for all props with proper descriptions
  - Accessibility testing integration with automated a11y checks
  - Responsive viewport testing across all breakpoints
  - Props table with TypeScript definitions and default values
  - Usage examples with code snippets
  - Do's and Don'ts section for each component
- **View Components Button**: Implement a custom Storybook addon/button that allows users to:
  - View component source code directly in Storybook
  - Copy component usage examples to clipboard
  - Navigate to component documentation
  - Export component props as JSON
  - Generate component usage snippets for different frameworks
- Create design system documentation pages with interactive examples
- Add visual regression testing with Chromatic
- Include performance benchmarks for each component
- Document component APIs with comprehensive prop tables and examples

### 6. Testing Strategy
- Unit tests using React Testing Library and Jest
- Visual regression testing with Storybook and Chromatic across all theme variations
- **Theme-Specific Testing**: Automated testing for all components across all 5 themes:
  - Light Theme compatibility testing
  - Dark Theme contrast validation
  - Pure White Theme accessibility compliance
  - True Black Theme OLED optimization verification
  - E-Commerce Dark Theme visual hierarchy testing
- Accessibility testing with axe-core and jest-axe for each theme variant
- Cross-browser testing setup with theme persistence verification
- Component interaction testing with theme switching scenarios
- Performance testing for theme switching and heavy components

### 7. Developer Experience
- Comprehensive TypeScript definitions
- IntelliSense support with JSDoc comments
- Codemods for breaking changes during updates
- Development playground for rapid prototyping
- Clear migration guides and changelogs
- ESLint plugin for enforcing best practices

### 8. Distribution & Publishing
- NPM package publishing with automated versioning
- CDN distribution for non-bundler usage
- Multiple output formats (ES modules, CommonJS, UMD)
- CSS extraction for styling flexibility
- Peer dependency management for React versions
- Documentation deployment to Netlify/Vercel

### 9. Quality Assurance
- Automated testing in CI/CD pipeline
- Code coverage requirements (minimum 80%)
- Bundle size monitoring and alerts
- Performance benchmarking
- Regular dependency updates and security audits
- Community contribution guidelines

### 10. Advanced Features (Future Enhancements)
- **Component Composition Utilities**: Higher-order components and render props for advanced composition
- **Advanced Theming System**: Multi-brand support, custom theme builder, and theme marketplace
- **Micro-Interactions**: Hover effects, click animations, and delightful transitions
- **Performance Optimization**: Component lazy loading, bundle splitting, and memory optimization
- **Accessibility Enhancements**: Screen reader optimization, keyboard shortcuts, and voice commands
- **Internationalization (i18n)**: Multi-language support with RTL theme variations and locale-specific formatting
- **Animation System**: Physics-based animations, gesture recognition, and scroll-triggered animations
- **Advanced Form Features**: Multi-step forms, conditional fields, auto-save, and form analytics
- **Real-time Features**: WebSocket integration, live updates, and collaborative editing
- **AI Integration**: Smart autocomplete, content suggestions, and accessibility improvements
- **Developer Tools**: Component inspector, design tokens manager, and usage analytics
- **Testing Utilities**: Component mocks, test helpers, and automated accessibility testing
- **Design System Management**: Version control for design tokens, component migration tools
- **Performance Monitoring**: Bundle analysis, runtime performance tracking, and optimization suggestions

## Deliverables
1. Complete React UI component library with TypeScript
2. **Comprehensive Storybook documentation site** featuring:
   - Individual stories for every UI component with complete documentation
   - Custom "View Components" button for enhanced developer experience
   - Interactive playground for testing component combinations
   - Theme switching interface within Storybook
3. **Five-Theme System Implementation**:
   - Light Theme (default)
   - Dark Theme (standard dark mode)
   - Pure White Theme (high contrast minimal)
   - True Black Theme (OLED optimized)
   - E-Commerce Dark Theme (premium shopping experience)
4. NPM package ready for distribution with theme support
5. Testing suite with high coverage across all themes
6. CI/CD pipeline configuration with theme validation
7. Migration and usage documentation including theming guides
8. Design system guidelines with theme specifications
9. Performance benchmarks and optimization reports for all theme variants

## Success Metrics
- Bundle size optimization: Core components under 100KB, full library under 500KB (excluding theme assets)
- **Storybook Coverage**: 100% of components have complete interactive documentation with live examples
- 100% accessibility compliance across all 5 theme variations and 150+ components
- Cross-browser compatibility (Chrome, Firefox, Safari, Edge) with theme persistence
- Mobile responsiveness across all target devices for all themes and components
- **Component Library Completeness**: 150+ production-ready components covering all common UI patterns
- **Theme Performance**: Sub-100ms theme switching across all components
- **E-Commerce Readiness**: Complete shopping experience component coverage
- Developer adoption with comprehensive documentation and examples
- Performance scores above 90 in Lighthouse audits for all theme variants
- **Community Engagement**: Active usage in production applications with positive developer feedback
