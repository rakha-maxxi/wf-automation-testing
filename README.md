# 🧪 Work Fusion — Maestro Automation Testing

Comprehensive end-to-end UI automation testing suite for the **Work Fusion** mobile application using [Maestro](https://maestro.mobile.dev/) framework.

## 📋 Project Overview

| Item | Detail |
|---|---|
| **App ID** | `com.sindika.workfusion` |
| **Framework** | Maestro (YAML-based) |
| **Platform** | Android / iOS |
| **Test Account (Worker)** | `rakha` / `Rakha123!` |
| **Test Account (Supervisor)** | `nailussaada` / `Nailus123!` |

---

## 📁 Folder Structure

```
wf-testing/
├── README.md                       # This file
├── RESULT.md                       # Test results documentation
│
├── auth/                           # 🔐 Authentication Module (8 tests)
│   ├── worker-login-success.yaml
│   ├── supervisor-login-success.yaml
│   ├── worker-login-empty-username.yaml
│   ├── worker-login-empty-password.yaml
│   ├── worker-login-invalid-credentials.yaml
│   ├── worker-logout.yaml
│   ├── verify-login-page-elements.yaml
│   └── verify-webview-auth-opens.yaml
│
├── home/                           # 🏠 Home / Overview Module (12 tests)
│   ├── verify-greeting-header.yaml
│   ├── verify-work-overview-section.yaml
│   ├── verify-today-task-section.yaml
│   ├── verify-bottom-navigation.yaml
│   ├── open-overview-filter.yaml
│   ├── apply-yesterday-filter.yaml
│   ├── apply-today-filter.yaml
│   ├── apply-this-week-filter.yaml
│   ├── apply-this-month-filter.yaml
│   ├── apply-custom-range-filter.yaml
│   ├── cancel-overview-filter.yaml
│   └── navigate-to-my-task-via-link.yaml
│
├── my-task/                        # 📋 My Task Module (28 tests)
│   ├── verify-correct-header.yaml
│   ├── verify-default-tab.yaml
│   ├── verify-ongoing-tab.yaml
│   ├── verify-switching-to-done-tab.yaml
│   ├── verify-done-tab-task-list.yaml
│   ├── verify-done-tab-empty-state.yaml
│   ├── verify-empty-state-for-ongoing-tab.yaml
│   ├── verify-search-input-field-is-visible.yaml
│   ├── verify-search-functionality.yaml
│   ├── verify-filter-button-area-renders.yaml
│   │
│   │   # Status Filter
│   ├── open-status-filter-bottom-sheet-via-first-filter.yaml
│   ├── select-draft-task-from-status-filter.yaml
│   ├── select-pending-task-from-status-filter.yaml
│   ├── select-overdue-task-from-status-filter.yaml
│   ├── select-need-approval-from-status-filter.yaml
│   ├── reset-status-filter-to-all-task.yaml
│   ├── close-status-filter-via-close-button.yaml
│   │
│   │   # Priority Filter
│   ├── open-priority-filter.yaml
│   ├── select-urgent-task-from-priority-filter.yaml
│   ├── select-low-task-from-priority-filter.yaml
│   ├── reset-priority-filter-to-all-priority.yaml
│   ├── close-priority-filter-via-close-button.yaml
│   │
│   │   # Due Date Filter
│   ├── open-due-date-filter.yaml
│   ├── select-today-from-due-date-filter.yaml
│   ├── select-this-week-from-due-date-filter.yaml
│   ├── select-this-month-from-due-date-filter.yaml
│   ├── select-custom-range-from-due-date-filter.yaml
│   └── close-due-date-filter-via-close-button.yaml
│
├── profile/                        # 👤 Profile Module (13 tests)
│   ├── verify-profile-page-header.yaml
│   ├── verify-profile-info-display.yaml
│   ├── verify-account-section-menu.yaml
│   ├── verify-general-section-menu.yaml
│   ├── verify-language-toggle.yaml
│   ├── navigate-to-edit-profile.yaml
│   ├── verify-update-profile-elements.yaml
│   ├── edit-profile-name-and-save.yaml
│   ├── back-from-update-profile.yaml
│   ├── verify-update-picture-options.yaml
│   ├── navigate-to-change-password.yaml
│   ├── verify-change-password-elements.yaml
│   └── back-from-change-password.yaml
│
├── notification/                   # 🔔 Notification Module (6 tests)
│   ├── verify-notification-page-header.yaml
│   ├── verify-notification-tabs.yaml
│   ├── switch-to-unread-tab.yaml
│   ├── switch-to-view-all-tab.yaml
│   ├── verify-mark-all-read-button.yaml
│   └── tap-mark-all-read.yaml
│
└── monitoring/                     # 📊 Monitoring Module (16 tests)
    ├── verify-monitoring-view.yaml
    ├── approve-task.yaml
    ├── reject-task.yaml
    ├── see-response-by-question.yaml
    ├── see-response-by-individual.yaml
    │
    │   # Status Filter
    ├── set-not-started-filter-monitoring.yaml
    ├── set-need-approval-filter-monitoring.yaml
    ├── set-partially-complete-filter-monitoring.yaml
    │
    │   # Priority Filter
    ├── set-priority-urgent-task-filter-monitoring.yaml
    ├── set-priority-normal-task-filter-monitoring.yaml
    ├── set-priority-low-task-filter-monitoring.yaml
    │
    │   # Due Date Filter
    ├── set-due-date-today-filter-monitoring.yaml
    ├── set-due-date-yesterday-filter-monitoring.yaml
    ├── set-due-date-this-week-filter-monitoring.yaml
    ├── set-due-date-this-month-filter-monitoring.yaml
    └── set-due-date-custom-range-filter-monitoring.yaml
```

---

## 📊 Test Summary

| Module | Total Tests | Category |
|---|:---:|---|
| **Auth** | 8 | Login, Logout, Negative tests, UI verification |
| **Home** | 12 | Dashboard, Greeting, Overview filter, Navigation |
| **My Task** | 28 | Tabs, Task list, Status/Priority/Due Date filters, Search |
| **Profile** | 13 | View, Edit, Change password, Navigation, UI elements |
| **Notification** | 6 | Tabs, Mark as read, Empty states |
| **Monitoring** | 16 | Supervisor RBAC, Status/Priority/Due Date filters, Task actions |
| **Total** | **83** | |

---

## 🚀 How to Run

### Run All Tests
```bash
maestro test wf-testing/
```

### Run a Single Module
```bash
maestro test wf-testing/auth/
maestro test wf-testing/home/
maestro test wf-testing/my-task/
maestro test wf-testing/profile/
maestro test wf-testing/notification/
maestro test wf-testing/monitoring/
```

### Run a Single Test
```bash
maestro test wf-testing/auth/worker-login-success.yaml
```

---

## 📌 Test Naming Convention

Files follow a **kebab-case** naming pattern:

| Pattern | Example |
|---|---|
| `{action}-{target}.yaml` | `worker-login-success.yaml` |
| `verify-{element}.yaml` | `verify-greeting-header.yaml` |
| `open-{component}.yaml` | `open-overview-filter.yaml` |
| `apply-{filter}.yaml` | `apply-yesterday-filter.yaml` |
| `select-{option}-from-{filter}.yaml` | `select-draft-task-from-status-filter.yaml` |
| `navigate-to-{page}.yaml` | `navigate-to-edit-profile.yaml` |
| `back-from-{page}.yaml` | `back-from-change-password.yaml` |

---

## 🔑 Key Concepts

### `clearState: true` vs `clearState: false`

| Setting | Use Case |
|---|---|
| `clearState: true` | Full fresh start — clears app data and requires login flow |
| `clearState: false` | Assumes user is already logged in — skips login steps |

### Test Categories

- **✅ Happy Flow** — Standard successful user journey (e.g., login success)
- **❌ Negative Test** — Invalid input validation (e.g., empty username)
- **🔍 UI Verification** — Assert UI elements exist and render correctly
- **🧭 Navigation** — Verify page transitions and routing
- **🔎 Filter/Search** — Test filter bottom sheets and search functionality
- **🔐 RBAC** — Role-based access control (e.g., Monitoring tab visibility)

---

## 📝 Notes

- Tests targeting **Worker** role use credentials: `rakha` / `Rakha123!`
- Tests targeting **Supervisor** role use credentials: `nailussaada` / `Nailus123!`
- The **Monitoring** tab is only visible for Supervisor roles
- Date-dependent tests (custom range filter) may need adjustment based on the current date
- Tests using `clearState: false` require a prior successful login session
