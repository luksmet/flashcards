# Product Requirements Document (PRD) - AI Flashcard Learning Platform (MVP)

## 1. Product Overview

The AI Flashcard Learning Platform is a web-based educational tool designed to streamline the creation and study of flashcards. For the MVP, the platform will focus on leveraging AI to generate high-quality flashcards from user-provided text, solving the problem of time-consuming manual creation.

Target users are primarily high school students (ages 13+) seeking an efficient way to prepare for tests. The platform combines AI-assisted content generation with a proven spaced repetition methodology (Leitner system) to optimize learning.

## 2. User Problem

Creating high-quality flashcards manually is a significant time investment that discourages students from using effective study methods like spaced repetition. This upfront effort detracts from actual study time and can lead to abandoning the method altogether. This platform aims to eliminate that initial friction.

## 3. Functional Requirements

### 3.1 User Authentication
- FR-001: The system shall support Google Sign-In as the sole authentication method.
- FR-002: The system shall maintain minimal user profiles containing a unique user ID, email, and display name.

### 3.2 Deck Management
- FR-003: Users shall be able to create named decks to organize flashcards.
- FR-004: Users shall be able to view a list of their created decks.

### 3.3 AI-Powered Flashcard Generation
- FR-005: The system shall accept user input consisting of a block of text (150-15,000 characters) and a desired number of flashcards.
- FR-006: The system shall generate flashcards in a question/answer format.
- FR-007: A monthly per-user limit on AI generations shall be enforced (configurable via database).

### 3.4 Flashcard Review Workflow
- FR-008: Each AI-generated card shall be presented for review with editable question and answer fields.
- FR-009: Users shall be able to "Accept" a card, saving it to their deck, or "Reject" a card, discarding it.
- FR-010: Accepted cards (whether edited or not) count toward the success metric. Rejected cards are stored separately for analysis.

### 3.5 Manual Flashcard Creation
- FR-011: Users shall be able to manually create flashcards with a question and answer.
- FR-012: Manually created cards shall be saved directly to a deck without a review step.

### 3.6 Study Sessions & Spaced Repetition
- FR-013: The system shall implement the Leitner system for spaced repetition scheduling.
- FR-014: A study session shall present the questions of cards due for review.
- FR-015: Users shall be able to reveal the answer and then indicate if they "knew it" or "didn't know it".
- FR-016: A summary screen shall be displayed at the end of the session showing performance counts.

## 4. Product Boundaries

### 4.1 Out of Scope for MVP
- Custom repetition algorithms (Leitner system only)
- File imports (text input only)
- Sharing decks between users
- Native mobile applications (web only)
- Administrative UI panel
- Sub-decks, deck renaming, deck deletion
- Bulk "Accept All" / "Reject All" actions

## 5. User Stories

### US-001: New User Authentication
- ID: US-001
- Title: New User Authenticates via Google Sign-In
- Description: As a new user, I want to sign in quickly using my Google account so that I can start using the application without creating a new password.
- Acceptance Criteria:
  - The login page presents a "Sign In with Google" button.
  - Clicking the button initiates the Google OAuth flow.
  - Upon successful authentication, a user profile is created in the system.
  - The user is logged in and redirected to the main dashboard.

### US-002: Deck Creation
- ID: US-002
- Title: User Creates a Deck
- Description: As a user, I want to create a named deck so that I can organize my flashcards by subject or topic.
- Acceptance Criteria:
  - There is an option to "Create New Deck" on the dashboard.
  - I am prompted to enter a name for the deck.
  - The new deck appears in my list of decks.

### US-003: AI-Powered Flashcard Generation
- ID: US-003
- Title: User Generates Flashcards from Text
- Description: As a user, I want to paste a block of text and specify a number of cards to generate, so that I can quickly create study materials without manual typing.
- Acceptance Criteria:
  - Within a deck, I can choose to generate cards with AI.
  - I can paste text into an input field (min 150 characters).
  - I can specify the number of cards I want.
  - Clicking "Generate" initiates the process and shows a loading state.
  - The system presents the generated cards for my review.

### US-004: Flashcard Review and Acceptance
- ID: US-004
- Title: User Reviews and Accepts AI-Generated Flashcards
- Description: As a user, I want to review each AI-generated flashcard to ensure its accuracy and relevance, with the ability to edit it before saving.
- Acceptance Criteria:
  - Each generated card is displayed one by one.
  - I can edit the question and answer text.
  - I can click an "Accept" button to save the card (with any edits) to my deck.
  - I can click a "Reject" button to discard the card.
  - Accepted cards are immediately available for studying.

### US-005: Manual Flashcard Creation
- ID: US-005
- Title: User Manually Creates a Flashcard
- Description: As a user, I want a simple way to manually create a single flashcard with a question and answer for specific terms not covered by the AI.
- Acceptance Criteria:
  - Within a deck, there is an option to "Create Manual Card".
  - A form is presented with fields for "Question" and "Answer".
  - After filling the fields and saving, the card is added directly to my deck.

### US-006: Study Session
- ID: US-006
- Title: User Studies a Deck of Flashcards
- Description: As a user, I want to study the flashcards in a deck using a spaced repetition system to learn the material effectively.
- Acceptance Criteria:
  - I can start a study session from a deck.
  - The system presents me with cards that are due for review.
  - For each card, the question is shown first.
  - I can click a button to reveal the answer.
  - After seeing the answer, I can select "I knew it" or "I didn't know".
  - My response determines the next time I will see the card.
  - At the end of the session, I see a summary of my performance.


## 6. Success Metrics

### 6.1 Primary Success Metrics

#### Metric 1: AI Flashcard Acceptance Rate
- Target: 75%
- Definition: (Accepted cards / Total generated cards) x 100. Accepted cards include both as-is and edited cards.
- Rationale: Measures the quality and usefulness of the AI generation feature. A high rate indicates users find the AI-generated content valuable.

#### Metric 2: AI Usage Rate
- Target: 75%
- Definition: (AI-generated cards / Total created cards) x 100.
- Rationale: Indicates whether the core AI feature is solving the user's problem and is preferred over manual creation.
