# ⚡ DHIS2 User Tools – Quick Start Guide (v1.0)

---

## Purpose

This **Quick Start Guide** provides a fast, practical overview for using the
**DHIS2 User Tools** app to explore **users, user roles, authorities, and user groups**
in a DHIS2 instance.

📘 For detailed explanations, screenshots, and governance guidance, refer to the
**Full User Guide**.

---

## Who This Guide Is For

This guide is intended for:
- DHIS2 system administrators
- Health informatics officers
- National / provincial HIS managers
- HISP support teams

You should already understand:
- DHIS2 User app
- User roles and authorities
- User groups

---

## What This App Does (At a Glance)

✅ View users assigned to a user role  
✅ Identify active vs. disabled users  
✅ Find which roles contain a specific authority  
✅ Review user group membership  
✅ Export user lists to CSV  

🚫 Does **not** modify users  
🚫 Does **not** change roles or authorities  

The app is **read-only** and safe for production use.

---

## App Sections

The app has **three main tabs**:

1. **User Role Viewer**
2. **User Authority Viewer**
3. **User Groups**

---

## Common Tasks (Quick Steps)

---

### Task 1: List users by user role

1. Open **User Role Viewer**
2. Select a **User role** from the dropdown
3. Review the user list
4. (Optional) Enable **Only active users**
5. Use pagination to navigate
6. Click **Export current list to CSV** if needed

---

### Task 2: Find disabled users in a role

1. Open **User Role Viewer**
2. Select a **User role**
3. Ensure **Only active users** is **unchecked**
4. Look at the **Status** column
   - *Active* = enabled
   - *Disabled* = login blocked

---

### Task 3: Find which roles contain a specific authority

1. Open **User Authority Viewer**
2. Select an **Authority category**
3. Search and select an **Authority**
4. Review the list of **User roles** that contain it

This is useful for:
- Security audits
- Privilege reviews
- Identifying over-privileged roles

---

### Task 4: Find users who indirectly have an authority

1. In **User Authority Viewer**, select an authority
2. Click **Show assigned users** for a role
3. The app switches to **User Role Viewer**
4. Review users assigned to that role

Workflow:
- Authority → Role → Users

---

### Task 5: Review user group membership

1. Open **User Groups**
2. Select a **User group**
3. Review the user list
4. Use pagination for large groups

---

### Task 6: Open a user in the DHIS2 User app

1. Locate the user in any list
2. Click **Open**
3. The user profile opens in the DHIS2 **User app** (new tab)

This is useful for:
- Profile review
- Enabling / disabling users
- Role changes (if authorized)

---

## CSV Export Notes

- CSV export downloads the **currently displayed page only**
- Includes:
  - Name
  - Username
  - Email
  - Status
  - Roles

📌 For full exports across many pages, export page-by-page or request an enhanced export feature.

---

## Best Practices

- Use **User Authority Viewer** for access and security audits
- Filter to **Only active users** when reviewing operational access
- Export CSV files and archive them for:
  - Quarterly access reviews
  - MoH / WHO audits
  - Change-management records

---

## Known Limitations (Quick)

- Fixed page size (default 50 users)
- CSV export is page-based
- Results depend on the logged-in user’s read permissions

---

## Support

**Application:** DHIS2 User Tools  
**Developer:** HISP Sri Lanka  

📘 Refer to the **Full User Guide** for complete documentation.

---

*End of Quick Start Guide*
