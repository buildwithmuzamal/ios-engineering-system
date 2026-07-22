# Phase 08 — Security

> **Purpose:** Learn to build secure iOS applications that protect user data, defend against common threats, and follow Apple's security recommendations.

---

# Goal

Develop the mindset that security is a fundamental engineering responsibility throughout the software lifecycle.

---

# Learning Outcomes

By the end of this phase you should be able to:

- Store sensitive data securely.
- Protect user privacy.
- Authenticate users safely.
- Understand common mobile security risks.
- Apply Apple's security best practices.

---

# Module 1 — Security Fundamentals

## Core Topics

- CIA Triad
- Threat Modeling
- Principle of Least Privilege
- Secure by Default

---

## Learning Objectives

After completing this module you should be able to:

- Understand CIA Triad and recognize when it is the right tool.
- Understand Threat Modeling and recognize when it is the right tool.
- Understand Principle of Least Privilege and recognize when it is the right tool.
- Understand Secure by Default and recognize when it is the right tool.
- Apply the module concepts in the mini project without copying a full solution.
- Use official documentation as the primary reference for this module.

---

## Parallel Learning Layers

### Git

- Never commit secrets or keychain material.
- Review diffs for accidental credential leaks.
- Keep security fixes isolated and reviewable.

### Xcode

- Keychain debugging caution
- Scheme environment variables
- Console redaction habits

### Apple Documentation

- Security overview
- Keychain Services
- App Privacy details

### WWDC

- Security and privacy sessions relevant to the module

### Best Practices

- Prefer clarity when working with CIA Triad.
- Keep responsibilities small and names meaningful.
- Validate understanding with a working example before moving on.

### Design Thinking

- What problem does CIA Triad solve?
- What would a simpler alternative look like?
- What trade-offs appear if this is overused?

### Architecture Thinking

- Where does this concept belong in a production app?
- What should stay out of the UI layer?
- How would this decision affect testing and change later?

### Open Source

- Study how an open-source app stores credentials

### AI

- Ask AI to explain CIA Triad after you attempt it yourself.
- Request a review of your design, not a full generated solution.
- Challenge AI suggestions against Apple documentation.

### English

- Write a short explanation of CIA Triad in your own words.
- Use precise terminology in notes and commit messages.
- Practice explaining trade-offs as you would in a pull request.

### Notes

- Document CIA Triad, Threat Modeling, Principle of Least Privilege, Secure by Default.
- Capture common mistakes and Apple recommendations.
- Link related modules and future spiral topics.

### Reflection

- Can I teach CIA Triad to another engineer?
- What is still unclear?
- How does this connect to previous phases?

---

## Mini Project

- Build a small focused exercise that proves you understand CIA Triad.
- Keep the scope small enough to finish, but realistic enough to reuse later.
- Document one design decision and one mistake you corrected.

---

## Exit Criteria

You should be able to:

- Use CIA Triad correctly in a realistic scenario and explain the trade-offs.
- Use Threat Modeling correctly in a realistic scenario and explain the trade-offs.
- Use Principle of Least Privilege correctly in a realistic scenario and explain the trade-offs.
- Use Secure by Default correctly in a realistic scenario and explain the trade-offs.
- Finish the mini project and describe one design decision you made.
- Write permanent notes covering the core topics, mistakes, and Apple guidance.
- Meet every Learning Objective for this module.


---

# Module 2 — Secure Storage

## Core Topics

- Keychain - Secure Enclave - UserDefaults vs Keychain - Sensitive

---

## Learning Objectives

After completing this module you should be able to:

- Understand Keychain - Secure Enclave - UserDefaults vs Keychain - Sensitive and recognize when it is the right tool.
- Apply the module concepts in the mini project without copying a full solution.
- Use official documentation as the primary reference for this module.

---

## Parallel Learning Layers

### Git

- Never commit secrets or keychain material.
- Review diffs for accidental credential leaks.
- Keep security fixes isolated and reviewable.

### Xcode

- Keychain debugging caution
- Scheme environment variables
- Console redaction habits

### Apple Documentation

- Security overview
- Keychain Services
- App Privacy details

### WWDC

- Security and privacy sessions relevant to the module

### Best Practices

- Prefer clarity when working with Keychain - Secure Enclave - UserDefaults vs Keychain - Sensitive.
- Keep responsibilities small and names meaningful.
- Validate understanding with a working example before moving on.

### Design Thinking

- What problem does Keychain - Secure Enclave - UserDefaults vs Keychain - Sensitive solve?
- What would a simpler alternative look like?
- What trade-offs appear if this is overused?

### Architecture Thinking

- Where does this concept belong in a production app?
- What should stay out of the UI layer?
- How would this decision affect testing and change later?

### Open Source

- Study how an open-source app stores credentials

### AI

- Ask AI to explain Keychain - Secure Enclave - UserDefaults vs Keychain - Sensitive after you attempt it yourself.
- Request a review of your design, not a full generated solution.
- Challenge AI suggestions against Apple documentation.

### English

- Write a short explanation of Keychain - Secure Enclave - UserDefaults vs Keychain - Sensitive in your own words.
- Use precise terminology in notes and commit messages.
- Practice explaining trade-offs as you would in a pull request.

### Notes

- Document Keychain - Secure Enclave - UserDefaults vs Keychain - Sensitive.
- Capture common mistakes and Apple recommendations.
- Link related modules and future spiral topics.

### Reflection

- Can I teach Keychain - Secure Enclave - UserDefaults vs Keychain - Sensitive to another engineer?
- What is still unclear?
- How does this connect to previous phases?

---

## Mini Project

- Store login credentials securely.
- Keep the scope small enough to finish, but realistic enough to reuse later.
- Document one design decision and one mistake you corrected.

---

## Exit Criteria

You should be able to:

- Use Keychain - Secure Enclave - UserDefaults vs Keychain - Sensitive correctly in a realistic scenario and explain the trade-offs.
- Finish the mini project and describe one design decision you made.
- Write permanent notes covering the core topics, mistakes, and Apple guidance.
- Meet every Learning Objective for this module.


---

# Module 3 — Authentication & Authorization

## Core Topics

- Biometrics - Face ID - Touch ID - OAuth concepts - Session

---

## Learning Objectives

After completing this module you should be able to:

- Understand Biometrics - Face ID - Touch ID - OAuth concepts - Session and recognize when it is the right tool.
- Apply the module concepts in the mini project without copying a full solution.
- Use official documentation as the primary reference for this module.
- Deepens Phase 05 Authentication with security and authorization mindset.

---

## Parallel Learning Layers

### Git

- Never commit secrets or keychain material.
- Review diffs for accidental credential leaks.
- Keep security fixes isolated and reviewable.

### Xcode

- Keychain debugging caution
- Scheme environment variables
- Console redaction habits

### Apple Documentation

- Security overview
- Keychain Services
- App Privacy details

### WWDC

- Security and privacy sessions relevant to the module

### Best Practices

- Prefer clarity when working with Biometrics - Face ID - Touch ID - OAuth concepts - Session.
- Keep responsibilities small and names meaningful.
- Validate understanding with a working example before moving on.

### Design Thinking

- What problem does Biometrics - Face ID - Touch ID - OAuth concepts - Session solve?
- What would a simpler alternative look like?
- What trade-offs appear if this is overused?

### Architecture Thinking

- Where does this concept belong in a production app?
- What should stay out of the UI layer?
- How would this decision affect testing and change later?

### Open Source

- Study how an open-source app stores credentials

### AI

- Ask AI to explain Biometrics - Face ID - Touch ID - OAuth concepts - Session after you attempt it yourself.
- Request a review of your design, not a full generated solution.
- Challenge AI suggestions against Apple documentation.

### English

- Write a short explanation of Biometrics - Face ID - Touch ID - OAuth concepts - Session in your own words.
- Use precise terminology in notes and commit messages.
- Practice explaining trade-offs as you would in a pull request.

### Notes

- Document Biometrics - Face ID - Touch ID - OAuth concepts - Session.
- Capture common mistakes and Apple recommendations.
- Link related modules and future spiral topics.

### Reflection

- Can I teach Biometrics - Face ID - Touch ID - OAuth concepts - Session to another engineer?
- What is still unclear?
- How does this connect to previous phases?

---

## Mini Project

- Protect a screen with biometrics.
- Keep the scope small enough to finish, but realistic enough to reuse later.
- Document one design decision and one mistake you corrected.

---

## Exit Criteria

You should be able to:

- Use Biometrics - Face ID - Touch ID - OAuth concepts - Session correctly in a realistic scenario and explain the trade-offs.
- Finish the mini project and describe one design decision you made.
- Write permanent notes covering the core topics, mistakes, and Apple guidance.
- Meet every Learning Objective for this module.


---

# Module 4 — Secure Networking

## Core Topics

- HTTPS - ATS - Certificate Pinning (concept) - Token handling

---

## Learning Objectives

After completing this module you should be able to:

- Understand HTTPS - ATS - Certificate Pinning (concept) - Token handling and recognize when it is the right tool.
- Apply the module concepts in the mini project without copying a full solution.
- Use official documentation as the primary reference for this module.

---

## Parallel Learning Layers

### Git

- Never commit secrets or keychain material.
- Review diffs for accidental credential leaks.
- Keep security fixes isolated and reviewable.

### Xcode

- Keychain debugging caution
- Scheme environment variables
- Console redaction habits

### Apple Documentation

- Security overview
- Keychain Services
- App Privacy details

### WWDC

- Security and privacy sessions relevant to the module

### Best Practices

- Prefer clarity when working with HTTPS - ATS - Certificate Pinning (concept) - Token handling.
- Keep responsibilities small and names meaningful.
- Validate understanding with a working example before moving on.

### Design Thinking

- What problem does HTTPS - ATS - Certificate Pinning (concept) - Token handling solve?
- What would a simpler alternative look like?
- What trade-offs appear if this is overused?

### Architecture Thinking

- Where does this concept belong in a production app?
- What should stay out of the UI layer?
- How would this decision affect testing and change later?

### Open Source

- Study how an open-source app stores credentials

### AI

- Ask AI to explain HTTPS - ATS - Certificate Pinning (concept) - Token handling after you attempt it yourself.
- Request a review of your design, not a full generated solution.
- Challenge AI suggestions against Apple documentation.

### English

- Write a short explanation of HTTPS - ATS - Certificate Pinning (concept) - Token handling in your own words.
- Use precise terminology in notes and commit messages.
- Practice explaining trade-offs as you would in a pull request.

### Notes

- Document HTTPS - ATS - Certificate Pinning (concept) - Token handling.
- Capture common mistakes and Apple recommendations.
- Link related modules and future spiral topics.

### Reflection

- Can I teach HTTPS - ATS - Certificate Pinning (concept) - Token handling to another engineer?
- What is still unclear?
- How does this connect to previous phases?

---

## Mini Project

- Secure API communication.
- Keep the scope small enough to finish, but realistic enough to reuse later.
- Document one design decision and one mistake you corrected.

---

## Exit Criteria

You should be able to:

- Use HTTPS - ATS - Certificate Pinning (concept) - Token handling correctly in a realistic scenario and explain the trade-offs.
- Finish the mini project and describe one design decision you made.
- Write permanent notes covering the core topics, mistakes, and Apple guidance.
- Meet every Learning Objective for this module.


---

# Module 5 — Privacy

## Core Topics

- App Privacy - Permissions - Photos - Camera - Location -

---

## Learning Objectives

After completing this module you should be able to:

- Understand App Privacy - Permissions - Photos - Camera - Location - and recognize when it is the right tool.
- Apply the module concepts in the mini project without copying a full solution.
- Use official documentation as the primary reference for this module.

---

## Parallel Learning Layers

### Git

- Never commit secrets or keychain material.
- Review diffs for accidental credential leaks.
- Keep security fixes isolated and reviewable.

### Xcode

- Keychain debugging caution
- Scheme environment variables
- Console redaction habits

### Apple Documentation

- Security overview
- Keychain Services
- App Privacy details

### WWDC

- Security and privacy sessions relevant to the module

### Best Practices

- Prefer clarity when working with App Privacy - Permissions - Photos - Camera - Location -.
- Keep responsibilities small and names meaningful.
- Validate understanding with a working example before moving on.

### Design Thinking

- What problem does App Privacy - Permissions - Photos - Camera - Location - solve?
- What would a simpler alternative look like?
- What trade-offs appear if this is overused?

### Architecture Thinking

- Where does this concept belong in a production app?
- What should stay out of the UI layer?
- How would this decision affect testing and change later?

### Open Source

- Study how an open-source app stores credentials

### AI

- Ask AI to explain App Privacy - Permissions - Photos - Camera - Location - after you attempt it yourself.
- Request a review of your design, not a full generated solution.
- Challenge AI suggestions against Apple documentation.

### English

- Write a short explanation of App Privacy - Permissions - Photos - Camera - Location - in your own words.
- Use precise terminology in notes and commit messages.
- Practice explaining trade-offs as you would in a pull request.

### Notes

- Document App Privacy - Permissions - Photos - Camera - Location -.
- Capture common mistakes and Apple recommendations.
- Link related modules and future spiral topics.

### Reflection

- Can I teach App Privacy - Permissions - Photos - Camera - Location - to another engineer?
- What is still unclear?
- How does this connect to previous phases?

---

## Mini Project

- Audit an app's permissions.
- Keep the scope small enough to finish, but realistic enough to reuse later.
- Document one design decision and one mistake you corrected.

---

## Exit Criteria

You should be able to:

- Use App Privacy - Permissions - Photos - Camera - Location - correctly in a realistic scenario and explain the trade-offs.
- Finish the mini project and describe one design decision you made.
- Write permanent notes covering the core topics, mistakes, and Apple guidance.
- Meet every Learning Objective for this module.


---

# Module 6 — Secure Coding

## Core Topics

- Input validation - Error handling - Defensive programming -

---

## Learning Objectives

After completing this module you should be able to:

- Understand Input validation - Error handling - Defensive programming - and recognize when it is the right tool.
- Apply the module concepts in the mini project without copying a full solution.
- Use official documentation as the primary reference for this module.

---

## Parallel Learning Layers

### Git

- Never commit secrets or keychain material.
- Review diffs for accidental credential leaks.
- Keep security fixes isolated and reviewable.

### Xcode

- Navigator
- Quick Help
- Breakpoints
- Documentation viewer

### Apple Documentation

- Official docs related to Input validation - Error handling - Defensive programming -

### WWDC

- Only sessions that directly strengthen this module

### Best Practices

- Prefer clarity when working with Input validation - Error handling - Defensive programming -.
- Keep responsibilities small and names meaningful.
- Validate understanding with a working example before moving on.

### Design Thinking

- What problem does Input validation - Error handling - Defensive programming - solve?
- What would a simpler alternative look like?
- What trade-offs appear if this is overused?

### Architecture Thinking

- Where does this concept belong in a production app?
- What should stay out of the UI layer?
- How would this decision affect testing and change later?

### Open Source

- Find a small open-source example related to Input validation - Error handling - Defensive programming -

### AI

- Ask AI to explain Input validation - Error handling - Defensive programming - after you attempt it yourself.
- Request a review of your design, not a full generated solution.
- Challenge AI suggestions against Apple documentation.

### English

- Write a short explanation of Input validation - Error handling - Defensive programming - in your own words.
- Use precise terminology in notes and commit messages.
- Practice explaining trade-offs as you would in a pull request.

### Notes

- Document Input validation - Error handling - Defensive programming -.
- Capture common mistakes and Apple recommendations.
- Link related modules and future spiral topics.

### Reflection

- Can I teach Input validation - Error handling - Defensive programming - to another engineer?
- What is still unclear?
- How does this connect to previous phases?

---

## Mini Project

- Build a small focused exercise that proves you understand Input validation - Error handling - Defensive programming -.
- Keep the scope small enough to finish, but realistic enough to reuse later.
- Document one design decision and one mistake you corrected.

---

## Exit Criteria

You should be able to:

- Use Input validation - Error handling - Defensive programming - correctly in a realistic scenario and explain the trade-offs.
- Finish the mini project and describe one design decision you made.
- Write permanent notes covering the core topics, mistakes, and Apple guidance.
- Meet every Learning Objective for this module.


---

# Phase Project

Improve an existing application by: - Moving secrets to Keychain. - Adding biometric authentication. - Reviewing permissions. - Securing networking. - Writing a security review document. - Creating a threat model.

---

# Exit Criteria

You are ready for the next phase when you can:

- Store sensitive information securely.
- Explain Apple's security model.
- Protect authentication data.
- Build privacy
- conscious features.
- Identify common security risks.

---

# Next Phase

➡️ Phase 09 — System Design
