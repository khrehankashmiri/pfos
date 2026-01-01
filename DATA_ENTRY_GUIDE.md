# PFOS - Data Entry & Editing Guide

## 📝 HOW TO ADD & EDIT DATA

### ✅ Quick Overview

PFOS now has **full data entry and editing capabilities**! You can:
- ✅ Add new expenses, tasks, and documents
- ✅ Edit existing entries
- ✅ Delete entries
- ✅ Mark tasks as complete
- ✅ All data is stored in the app (ready for database integration)

---

## 💰 ADDING & EDITING EXPENSES

### To Add a New Expense:

1. **Click "Add Expense" button** in the header
2. **Fill in the form:**
   - **Amount** (required) - Enter the expense amount
   - **Currency** (required) - Choose from:
     - USD (US Dollar)
     - EUR (Euro)
     - GBP (British Pound)
     - PKR (Pakistani Rupee)
     - INR (Indian Rupee)
     - SCU (Site Cash Units) - Custom currency
     - FCU (Family Currency Units) - Custom currency
   - **Category** (required) - Select from:
     - Food, Utilities, Transport, Health, Education
     - Entertainment, Shopping, Bills, Other
   - **Description** (required) - What was this expense for?
   - **Date** (required) - When did this expense occur?
   - **Shared With** (optional) - Select family members who share this expense
3. **Click "Save Expense"**

### To Edit an Expense:

1. Find the expense in the "Recent Expenses" section
2. Click the **✏️ Edit button**
3. Modify any fields
4. Click "Update Expense"

### To Delete an Expense:

1. Find the expense in the "Recent Expenses" section
2. Click the **🗑️ Delete button**
3. Confirm deletion

### Preview Feature:
- As you type the amount, you'll see a **live preview** showing:
  - Currency symbol + amount
  - Full currency name

**Example:**
```
Amount: 500
Currency: SCU
Preview: "SCU500 (Site Cash Units)"
```

---

## ✓ ADDING & EDITING TASKS

### To Add a New Task:

1. **Click "Add Task" button** in the header
2. **Fill in the form:**
   - **Title** (required) - What needs to be done?
   - **Type** (required) - Choose:
     - Task - Regular to-do item
     - Appointment - Scheduled meeting/event
     - Reminder - Simple reminder
   - **Priority** (required) - Choose:
     - Low - Can wait
     - Medium - Should be done soon
     - High - Urgent/important
   - **Due Date** (required) - When is this due?
   - **Status** (required) - Choose:
     - Pending - Not started
     - In-progress - Currently working on it
     - Done - Completed
   - **Description** (optional) - Add more details
   - **Assigned To** (optional) - Select family members
3. **Click "Save Task"**

### To Edit a Task:

1. Find the task in the "Pending Tasks" section
2. Click the **✏️ Edit button**
3. Modify any fields
4. Click "Update Task"

### To Complete a Task:

1. Find the task in the "Pending Tasks" section
2. Click the **✓ Complete button**
3. Task status changes to "Done" and moves out of pending list

### To Delete a Task:

1. Find the task in the "Pending Tasks" section
2. Click the **🗑️ Delete button**
3. Confirm deletion

### Priority Badges:
- **High** - Red badge (urgent)
- **Medium** - Orange badge (important)
- **Low** - Blue badge (can wait)

---

## 📄 ADDING & EDITING DOCUMENTS

### To Add a New Document:

1. **Click "Add Document" button** in the header
2. **Fill in the form:**
   - **Document Title** (required) - e.g., "My Passport"
   - **Document Type** (required) - Choose from:
     - Passport, Visa, Driver License, ID Card
     - Insurance, Contract, Certificate
     - Invoice, Receipt, Other
   - **Document Number** (optional) - e.g., "AB1234567"
   - **Issue Date** (optional) - When was it issued?
   - **Expiry Date** (required) - When does it expire?
   - **Issuing Authority** (optional) - e.g., "Government of Pakistan"
   - **Tags** (optional) - Add custom tags for organization
   - **Notes** (optional) - Additional information
3. **Click "Save Document"**

### Expiry Alert System:
The form automatically calculates days until expiry and shows color-coded alerts:

- **🔴 Red Alert** - Expires in < 30 days (Critical)
- **🟠 Orange Alert** - Expires in 30-90 days (Warning)
- **🔵 Blue Alert** - Expires in > 90 days (Info)
- **⚠️ Expired** - Shows days since expiration

**Example:**
```
Expiry Date: 2024-12-15
Alert: "⏰ Expires in 25 days" (Red - Critical)
```

### To Add Tags:

1. Type a tag name in the "Tags" field
2. Press **Enter** or click **Add** button
3. Tag appears as a colored badge
4. Click **×** on any tag to remove it

### To Edit a Document:

1. Find the document in the "Upcoming Expiries" section
2. Click the **Edit button**
3. Modify any fields
4. Click "Update Document"

---

## 🎨 CUSTOMIZING YOUR DASHBOARD

### To Show/Hide Widgets:

1. **Click "Customize" button** in the header
2. **Check/uncheck widgets:**
   - ✅ Upcoming Expiries
   - ✅ Pending Tasks
   - ✅ Recent Expenses
   - ✅ Summary Cards
   - ✅ Analytics Charts
3. Dashboard updates instantly

---

## 📊 FILTERING & EXPORTING DATA

### Date Range Filter:
- **Today** - Show only today's data
- **This Week** - Last 7 days
- **This Month** - Current month
- **This Year** - Current year
- **Custom Range** - Choose specific dates (coming soon)

### Category Filter:
- **All** - Show everything
- **Documents** - Only documents
- **Finance** - Only expenses
- **Tasks** - Only tasks
- **Vault** - Only vault items

### Export Reports:
Click any export button to generate reports:
- **📊 Export PDF** - Full report with charts
- **📈 Export Excel** - Spreadsheet format
- **📋 Export CSV** - Raw data

---

## 💡 PRO TIPS

### Multi-Currency Support:
- Use **SCU (Site Cash Units)** for construction site payments
- Use **FCU (Family Currency Units)** for internal family budgeting
- Mix currencies freely - the system tracks them separately

### Family Sharing:
- Check "Shared With" boxes to split expenses
- Assign tasks to family members
- Track who owes what

### Document Organization:
- Use **tags** to group related documents
- Add **notes** for important details
- Set **expiry dates** to get automatic alerts

### Task Management:
- Use **High priority** for urgent items
- Use **Appointments** for time-specific events
- Use **Reminders** for simple notifications

---

## 🔄 DATA FLOW

### Current Implementation:
```
User Input → Form → React State → Dashboard Display
```

### Future Implementation (Phase 2):
```
User Input → Form → React State → SQLite Database → Cloud Sync (Optional)
```

---

## 🎯 KEYBOARD SHORTCUTS (Coming Soon)

- **Ctrl + E** - Add Expense
- **Ctrl + T** - Add Task
- **Ctrl + D** - Add Document
- **Ctrl + S** - Save Form
- **Esc** - Close Form

---

## 📱 MOBILE SUPPORT

All forms are **fully responsive** and work on:
- ✅ Desktop (Windows, Mac, Linux)
- ✅ Tablets (iPad, Android tablets)
- ✅ Mobile phones (iOS, Android)

---

## 🔐 DATA SECURITY

### Current Status:
- Data stored in browser memory (React state)
- Persists during session
- Resets on page refresh

### Phase 2 (Coming Soon):
- SQLite database (local storage)
- Encrypted vault for sensitive data
- Optional cloud backup (encrypted)

---

## 🆘 TROUBLESHOOTING

### Form Won't Open:
- Check browser console for errors
- Refresh the page
- Clear browser cache

### Data Not Saving:
- Ensure all required fields are filled
- Check for validation errors (red borders)
- Try again after refreshing

### Can't Edit/Delete:
- Make sure you're clicking the correct button
- Check if the item still exists
- Refresh the page

---

## 📝 FORM VALIDATION

All forms include **automatic validation**:

### Required Fields:
- Marked with ***** (asterisk)
- Cannot submit without filling these
- Red border appears if empty

### Date Validation:
- Must be valid date format
- Expiry dates show countdown
- Past dates allowed for historical data

### Number Validation:
- Amount must be positive number
- Decimals allowed (e.g., 123.45)
- Currency symbol added automatically

---

## 🎉 WHAT'S WORKING NOW

✅ **Add** expenses, tasks, documents
✅ **Edit** any existing entry
✅ **Delete** with confirmation
✅ **Complete** tasks
✅ **Multi-currency** support
✅ **Family sharing** checkboxes
✅ **Priority levels** for tasks
✅ **Expiry alerts** for documents
✅ **Tags** for organization
✅ **Live preview** for amounts
✅ **Responsive design** for all screens
✅ **Form validation** for data integrity

---

## 🔜 COMING SOON

🔄 **Database Integration** - Persistent storage
🔄 **File Upload** - Attach document scans
🔄 **OCR** - Extract text from images
🔄 **Recurring Expenses** - Auto-add monthly bills
🔄 **Task Reminders** - Email/SMS notifications
🔄 **Cloud Sync** - Access from anywhere
🔄 **Family Accounts** - Multi-user support

---

## 🚀 GET STARTED NOW!

1. Open the PFOS dashboard
2. Click any **"Add..."** button
3. Fill in the form
4. Click **"Save"**
5. See your data appear instantly!

---

**Need help?** All forms have helpful placeholders and tooltips!

**Status: ✅ FULLY FUNCTIONAL**

All data entry and editing features are working and ready to use!