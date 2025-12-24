# DHIS2 User Tools – User Guide (v1.0)

**Application:** DHIS2 User Tools  
**Developer:** HISP Sri Lanka  
**App version:** 1.2.2  
**Description:** DHIS2 app: user role and authority viewer with filters, pagination, searchable authority dropdown and CSV export. Optimized for DHIS2 2.42.

---

## 1. Introduction

**DHIS2 User Tools** is a lightweight administrative utility that helps you explore and review **users, user roles, system authorities, and user groups** within a DHIS2 instance.

The app is intended for:
- access reviews and audits
- troubleshooting user access issues
- governance and routine DHIS2 administration support

> **Important:** This app is **read-only**. It does not modify users, roles, authorities, or groups.

---

## 2. Intended Users

This application is intended for:
- DHIS2 system administrators
- health informatics officers
- national / provincial HIS managers
- HISP implementers and support teams

Users should already be familiar with:
- DHIS2 User app (Users & User Roles)
- basic concepts of user roles, authorities, and user groups

---

## 3. Prerequisites

### 3.1 DHIS2 requirements
- DHIS2 version **2.38+** (optimized for 2.42)
- App installed through **App Management**

### 3.2 Required permissions (read access)
The logged-in user must have permission to read:
- Users
- User roles
- User groups
- Authorities

> Superuser is fully supported and recommended for system-wide audits.

---

## 4. Application Overview

The app UI contains **three tabs**:

1. **User Role Viewer** – list users assigned to a selected user role, with filter, pagination, CSV export, and quick access to the DHIS2 User app.
2. **User Authority Viewer** – search authorities and identify user roles that contain a selected authority; then navigate to users.
3. **User Groups** – list users in a selected user group, with pagination.

---

## 5. User Role Viewer

### 5.1 Purpose

Use this tab to:
- select a **User Role**
- view assigned users
- filter to **Only active users**
- export the current page to CSV
- open a user directly in the DHIS2 User app

### 5.2 Select a user role

1. Open the **User Role Viewer** tab.
2. In the **User role** dropdown, select the required role.
3. The app loads users assigned to that role.

If no role is selected, the app shows: **“No role selected.”**

### 5.3 User list table

For each user, the table displays:

| Column | Description |
|---|---|
| Name | User display name |
| Username | Login username |
| Email | Email address (if available) |
| Roles | User roles assigned to the user (shown as chips) |
| Status | **Active** or **Disabled** |
| Action | **Open** (opens user in DHIS2 User app) |

**Status meaning:**
- **Active** – user account is enabled
- **Disabled** – user cannot log in (disabled flag in user credentials)

### 5.4 Filter: Only active users

Enable **Only active users** to remove disabled accounts from the list.

Notes:
- When enabled, the app fetches the full role user list (no paging) and filters locally.
- Pagination still applies after filtering.

### 5.5 Pagination

- Page size is **50 users** by default.
- Use **Previous** / **Next** to move between pages.
- Page info shows:
  - current page number
  - total pages
  - number of users shown vs total found

### 5.6 Export current list to CSV

Click **Export current list to CSV** to download the **currently displayed page**.

The exported CSV includes:
- Name
- Username
- Email
- Status
- Roles (joined with ` | `)

**Tip:** For a complete role export across all pages, export each page and merge files externally (or request an enhanced “export all pages” feature).

### 5.7 Open user in DHIS2 User app

Click **Open** to open the selected user in the DHIS2 **User app** in a new browser tab.

Typical uses:
- quick profile review
- enabling/disabling users (if authorized)
- role adjustments (if authorized)

---

## 6. User Authority Viewer

### 6.1 Purpose

Use this tab to answer:

> “Which user roles contain a specific authority?”

This is useful for:
- privilege audits
- checking sensitive permissions (system admin, import, tracker, etc.)
- understanding access configuration

### 6.2 Select an authority category

1. Open **User Authority Viewer** tab.
2. Select an **Authority category**.

Categories are grouped logically (examples):
- Metadata authorities
- Available app authorities
- Available tracker authorities
- Available import/export authorities
- Available system authorities
- Legacy and nonstandard authorities

After selecting a category, the authority search box becomes active.

### 6.3 Search and select an authority

1. Click the **Authority** search box.
2. Start typing (search matches **authority id** and **authority name**).
3. Select an authority from the dropdown list.

If no authorities match, the dropdown shows: **“No authorities match your search.”**

### 6.4 View user roles containing the authority

After selecting an authority:
- the app lists all **user roles** that include that authority
- roles are sorted alphabetically

For each role, you can click:
- **Show assigned users**

### 6.5 Navigate to users of a role

When you click **Show assigned users**:
- the app switches to **User Role Viewer**
- selects the role automatically
- loads users for that role

This provides a simple workflow:
- Authority → Roles → Users → (Open user in DHIS2 User app)


---

## 7. User Groups

### 7.1 Purpose

Use this tab to:
- select a **User Group**
- list users assigned to that group
- review group membership

### 7.2 Select a user group

1. Open **User Groups** tab.
2. Choose a group from the dropdown.
3. Users are loaded and displayed.

If no group is selected, the app shows: **“No user group selected.”**

### 7.3 Group members table

The table is the same format as in User Role Viewer:
- Name, Username, Email, Roles, Status, Open

### 7.4 Pagination

- Same pagination controls as User Role Viewer
- Uses server paging for performance

---

## 8. API / System Behaviour Notes (For Administrators)

The app automatically derives the DHIS2 API base path so it works under different contexts such as:
- `/`
- `/dhis2`
- `/erhmis2`

This helps when DHIS2 is hosted under a sub-path.

---

## 9. Best Practices

- Use **User Authority Viewer** for privilege audits (find high-risk authorities → roles → users).
- Use **Only active users** to exclude disabled accounts during reviews.
- Export CSV results as evidence for:
  - access audits
  - quarterly reviews
  - change management

---

## 10. Known Limitations

- CSV export is for the **current page** only.
- Page size is fixed at **50** (by default).
- Authority categories are derived from authority naming conventions and may not perfectly match all custom authorities.
- Read permissions apply: if the logged-in user cannot read some objects, results may be incomplete.

---

## 11. Support and Maintenance

**Developer:** HISP Sri Lanka  
**Application:** DHIS2 User Tools  

For enhancements, bug fixes, or training:
- Coordinate with HISP Sri Lanka
- Align changes with DHIS2 upgrade cycles

---

*End of User Guide*

