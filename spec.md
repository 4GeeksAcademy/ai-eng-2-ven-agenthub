## SPEC.md## 1. Product Description
AgentHub is a centralized administrative control center designed for managing AI agents, system capabilities, client contracts, and diagnostic logs. The primary administrative user is an operations manager or platform administrator who monitors platform health, configures agent behaviors, reviews contractual usage, and troubleshoots runtime errors.
------------------------------
## 2. Tech Stack & Constraints

* Core Structure: Vanilla HTML5 using semantic elements (section, table, main, nav, etc.).
* Styling: Tailwind CSS injected via official CDN.
* Interactivity: Pure Vanilla JavaScript only.
* Strict Constraints: No JavaScript frameworks (React, Vue, Angular), no jQuery, no build tools, no external CSS files, and no inline style="" attributes.
* Data Handling: Fully hardcoded client-side mock data; no active backend connections or API endpoints.

------------------------------
## 3. Section Specifications## 3.1 Dashboard

   1. Metric Grid Layout: Contains four distinct metric cards arranged in a responsive 2x2 grid on mobile view scaling to a 1x4 horizontal row on desktop view.
   2. Visual Indicators: Each metric card features a unique accent background color per metric type, a distinct icon placeholder, a bolded text label, and a subtle drop shadow (shadow-sm).
   3. Activity Chart Placeholder: Features a full-width container (div) beneath the metric grid featuring a dashed border and a centered text label simulating a "Weekly Activity Chart".

## 3.2 User Management

   1. User Data Table: Displays a structured data table listing registered users with columns specifically for User Name, Email, Subscription Plan, and Account Status.
   2. Contextual Row Dropdowns: Every row includes an action button (⋮) that reveals a hidden absolute-positioned dropdown menu containing "View detail" and "Delete" actions.
   3. User Profile Modal: Clicking "View detail" triggers a center-aligned modal overlay displaying complete profile attributes. The modal must dismiss smoothly when clicking the background backdrop or an explicit close button.

## 3.3 Agent Management

   1. Agent Roster Grid: Displays a collection of at least 4 individual agent cards containing the Agent Name, Owner/Creator, Status Badge (Active, Inactive, Failing), and a summary list of assigned skills.
   2. Smooth Collapsible Skills: Skill details are collapsed by default; clicking an expand trigger reveals the extended skill checklist using transition classes (transition-all duration-300).
   3. Prompt Configuration Modal: The action dropdown contains a "Configure" option which invokes a modal window displaying an editable textarea populated with the agent's system prompt instructions.

## 3.4 Skills Catalog

   1. Contextual Header Panel: Features a brief summary paragraph at the top of the view explaining what platform "skills" represent and how they modulate agent behaviors.
   2. Capability Cards: Displays a minimum of 4 unique platform capabilities detailing the specific Skill Name, a brief technical description, and an interactive badge showing the exact count of active agents utilizing it.
   3. Management Controls: Each capability card contains an action dropdown providing options to view granular technical parameters or remove the capability from the global catalog.

## 3.5 Agent Contracts

   1. Financial Ledger Table: A high-density table displaying active and archived client-agent deployment agreements.
   2. Granular Column Layout: Tables must display explicitly: Client Name, Rented Agent, List of Contracted Skills, Activation/Expiration Dates, and Total Amount Paid.
   3. Itemized Billing Modal: Clicking "View detail" from the row action dropdown opens a modal showing an itemized invoice breakdown detailing individual skill pricing metrics.

## 3.6 Error Log

   1. Diagnostic Audit Stream: A chronological row-by-row stream displaying precise error timestamps, culprit Agent Name, Error Type classification, and a short message string.
   2. Severity Color Badges: Error entries are visually categorized using Tailwind utility badges color-coded by severity level (e.g., Red for Critical Runtime Failures, Yellow for Warnings).
   3. Resolution Tracking: Each entry contains a menu option to open a full error stack trace modal, alongside a "Mark as resolved" action button that updates state indicators.

------------------------------
## 4. Component Inventory

* Persistent Sidebar Navigation: Side menu holding section navigation links with state indicators for active/inactive views.
* Global Top Bar: Header area containing the primary workspace title and the central light/dark mode configuration toggle.
* Metric Card: A repeatable box component displaying a numeric data point, text label, and visual identifier.
* Action Dropdown Menu: An absolute-positioned menu toggleable by clicking a table row's options indicator (⋮).
* Modal Overlay: A full-screen backdrop overlay containing a centered, focus-locked content dialogue panel.
* Status Badge: Inline micro-containers utilizing colored background utility tokens indicating operational states or error classifications.
* Collapsible Container: An interactive element that toggles content visibility transitions when clicked.

------------------------------
## 5. Acceptance Criteria

   1. Spec Initialization: The SPEC.md file must be successfully committed to the repository root prior to authoring any workspace HTML files.
   2. Semantic Layout Integrity: The single-page layout must utilize valid semantic HTML markup tags (section, table, nav, main) throughout.
   3. Responsive Presentation: All views must maintain proper alignment, spacing, and text readability across standard mobile, tablet, and widescreen desktop breakpoints.
   4. Persistent Theme State: The global theme toggle must successfully alternate system elements between dark and light variants via Tailwind's dark: classes, preserving the state across navigation changes.
   5. Interactive Dropdown Isolation: Clicking a table row action trigger must display its local dropdown menu cleanly without opening adjacent menus; clicking outside the boundary closes it automatically.
   6. Interactive Modal Behavior: All modal views must initialize perfectly centered over the interface, block interaction with underlying elements, and close reliably upon background backdrop click.
   7. Consistent Mock Integrity: Hardcoded entities must remain visually synchronous across distinct sections (e.g., an identical failing agent must retain identical names across Agent Management, Contracts, and the Error Log).

------------------------------
## 6. Design theme and layout
1. Build as a single index.html file.
2. Dark theme color scheme
3. pre-populate specific mock agent names and skills for the hardcoded data structures.


