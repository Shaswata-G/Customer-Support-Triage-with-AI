# **GitHub Repository: Customer-Support-Triage-AI**

**Repository Name:** `customer-support-triage-ai`
**Tagline:** AI-powered support ticket triage workflow using n8n, Gmail, and Slack

---

## **1. Repository Description (GitHub “About”)**

> Automate your customer support with AI: incoming tickets are automatically categorized (Refund, Billing, Technical, General) and routed to the right team channel in Slack. Built with n8n, Gmail, and Slack for fast, efficient, and intelligent support operations. Ideal for SMBs, startups, and agencies looking to save time and reduce human error.

---

## **2. Suggested Project Structure**

```
customer-support-triage-ai/
│
├─ README.md
├─ LICENSE
├─ workflow/
│   └─ customer-support-triage.json   # Exported n8n workflow
├─ assets/
│   ├─ diagram.png                     # Workflow diagram
│   ├─ demo_gif1.gif                   # Demo: Email triggers workflow
│   ├─ demo_gif2.gif                   # Demo: Slack notification
│   └─ screenshots/                     # Optional screenshots
├─ docs/
│   └─ setup.md                        # Detailed setup guide
└─ examples/
    ├─ test_email_refund.eml           # Sample email
    ├─ test_email_billing.eml
    └─ test_email_technical.eml
```

---

## **3. README.md (Professional Version)**

```markdown
# Customer Support Triage with AI 🚀

Automate your support workflow with AI. Incoming emails are classified by type (Refund, Billing, Technical Issue, General Inquiry) and routed to the right Slack channel, reducing response time and manual errors.

![Workflow Diagram](assets/diagram.png)

---

## Why This Workflow?

- **Save Time:** Automates ticket triage, routing, and acknowledgment.
- **Reduce Errors:** AI categorization ensures tickets go to the correct team.
- **Professional Demo:** Great showcase for n8n, AI, and automation skills.

---

## 🛠️ Workflow Overview

**Workflow Flow:**

```

\[Gmail Trigger] --> \[Set Node: Extract Email] --> \[OpenAI Node: Categorize Ticket]
\--> \[Switch Node: Route by Category] --> \[Slack Node / ClickUp / Trello]
\--> \[Optional: Auto-Reply Email]

````

1. **Gmail Trigger:** Detects new support emails.  
2. **Set Node:** Cleans and structures email data.  
3. **OpenAI Node:** Categorizes ticket automatically.  
4. **Switch Node:** Routes tickets to the correct channel based on category.  
5. **Slack Node / ClickUp / Trello:** Sends notification or creates a task.  
6. **Optional Email Node:** Sends acknowledgment to the customer.

---

## ⚙️ Setup & Configuration

1. **Install n8n**  
   ```bash
   npm install n8n -g
   n8n start
````

2. **Connect Gmail Node**

   * OAuth2 setup
   * Trigger on a specific label/folder (e.g., `support@yourcompany.com`)
3. **Connect OpenAI Node**

   * Use your API key
   * Prompt for ticket classification:

     ```
     Classify this support ticket into one of the following categories: Refund, Billing, Technical Issue, General Inquiry. 
     Return only the category.
     Ticket: {{$json["ticket_body"]}}
     ```
4. **Configure Switch Node**

   * Branch by category to Slack/ClickUp/Trello nodes
5. **Connect Slack Node**

   * OAuth setup
   * Channels per category: `#refunds`, `#billing-support`, `#tech-support`, `#general-support`
6. **Optional: Email Auto-Reply**

   * Gmail Node → polite acknowledgment using structured email template

---

## ✅ Testing

* Use the sample emails in `/examples/` folder.
* Example: `test_email_refund.eml`
* Send the test email → check Slack notification → verify correct routing.

---

## 📸 Demo Ideas for README

1. **GIF:** Send a test email → Slack notification appears in the correct channel.
2. **GIF:** OpenAI Node categorization in real-time showing category output.
3. **Screenshot:** Workflow diagram in n8n with nodes highlighted and labeled.

---

## 📂 Assets & Diagram

* `assets/diagram.png`: Visual workflow showing Gmail → AI → Switch → Slack.
* `assets/demo_gif1.gif`: Email triggers workflow.
* `assets/demo_gif2.gif`: Ticket routed to Slack channel.

---

## 📄 License

This project is licensed under the **MIT License** – free to use, modify, and showcase for portfolio purposes. For commercial or production usage, please contact me.

---

> This workflow is designed to demonstrate automation expertise using n8n, AI, and SaaS integrations. Perfect for clients looking to streamline customer support operations.

```

---

## **4. Diagram Suggestion**
- A clean **PNG flow diagram** with arrows:  
```

Gmail → Set Node → OpenAI → Switch Node → Slack / ClickUp / Trello

```
- Use **colored nodes** to differentiate triggers, AI processing, routing, and notifications.  
- Tools: Lucidchart, Figma, or even draw.io.

---

## **5. Demo GIF / Screenshot Ideas**
1. **Send a test “Refund” email** → Slack channel receives the ticket notification.  
2. **OpenAI Node output** → showing JSON category result.  
3. **n8n workflow screen capture** → hover over each node with labels for visual clarity.

---

This setup will give clients a **professional, polished portfolio piece** that’s visually impressive and easy to understand.  

---

I can also **generate the workflow diagram PNG and sample demo GIF storyboard ideas** for your README so it’s ready to plug in.  

Do you want me to do that next?
```
