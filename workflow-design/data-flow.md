This diagram represents the **Level 0 Data Flow Diagram (DFD)** of the **AquaGuard System**.

The **AquaGuard System** is the central platform that connects three main entities:

1. **Community Users**

   * Users can submit water-related issues through SMS, phone, or email.
   * They can view the heat map of reported issues.
   * They can track the status of their submitted reports.

2. **Community Moderators**

   * Moderators log into the system.
   * They review and validate reported issues.
   * They manage pending reports and make approval or rejection decisions.

3. **Water Authority**

   * Receives validated reports from the system.
   * Takes action to resolve water-related issues.
   * Sends resolution updates back to the system.
   * The system sends alert notifications (via SMS or email) to concerned parties.

  **Overall Flow**

* Users report issues → AquaGuard System processes them.
* Moderators verify the reports.
* Approved issues are forwarded to the Water Authority.
* The authority resolves the issue and updates the system.
* Notifications and status updates are sent back to users.





This diagram represents the **Level 1 (Detailed) Data Flow Diagram** of the **AquaGuard System**, showing how a water issue report moves through different phases.

### 1️⃣ Submission Phase

* **Community Users** submit water-related complaints.
* The report is stored in the **Central Database** with a **“Pending”** status.
* The system waits for moderator review.

### 2️⃣ Moderation Phase

* A **Moderator** logs in through authentication and enters a secure PIN.
* The moderator reviews the complaint in the **Report Validation** step.
* If needed, **Technical Support** assists with authentication issues.
* The moderator then either **approves** or **rejects** the report.

### 3️⃣ Approval Branch (If Approved)

* The system updates the status to **Validated**.
* The **Heat Map** is updated to reflect the reported issue.
* The issue becomes visible on the **Public Interface** for community awareness.

### 4️⃣ Notification Branch (If Approved)

* The **Notification Service** sends alerts to the relevant **Authorities**.
* Authorities take action based on the validated complaint.

### 5️⃣ Rejection Case

* If rejected, the report is not forwarded and may be returned or closed.

### Overall Flow:

User submits report → Stored in database → Moderator validates →
If approved → Public update + Authorities notified → Action taken.

In simple terms, this diagram shows the step-by-step internal workflow of how AquaGuard processes, verifies, publishes, and escalates water issue reports.




