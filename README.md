# Invoice Approval Room: DevTools Academy "Flip the Script" Hackathon 2026

An AI agent and a human manager review invoices together inside a **Switch Room**. The whole workflow happens in the room.

## How it works
1. A user pastes invoice details into the `invoice-approvals` room and mentions `@invoice-approver2`.
2. The agent reads the invoice, checks the math, and flags anything unusual (wrong totals, duplicates, changed bank details, urgency pressure).
3. The agent asks the manager to reply **APPROVE** or **REJECT**.
4. The manager replies in the same room, and the agent confirms the decision.

## How Switch is used
- Switch Rooms provide the shared chat between the human and the agent.
- The agent (`invoice-approver2`) is added to the room and responds to mentions.
- The approve/reject decision happens only in the room. Nothing runs outside it.

## Setup
1. Install Switch Console and start the local Switch server.
2. Install and start **Docker Desktop** (needed for Room chat).
3. On Windows, turn on **Developer Mode** (Settings > Developer settings) so agent sessions can create symlinks.
4. Create a room named `invoice-approvals` and add an agent named `invoice-approver2`.
5. Paste the contents of `agent-instructions.md` into the agent's instructions.

## Try it
Paste the contents of `sample_invoice.pdf` as text into the room:

`@invoice-approver2 please review this invoice and flag anything unusual`

The sample invoice has a deliberate wrong total (95,830 instead of 21,830), a same-day due date, and a changed bank account.

## Known limitations
- Invoices are pasted as text. PDF attachments are not read by the agent yet.

## Demo
https://youtu.be/ukTS4AO6pJo?si=-IAbH_3lT19rLCot

## Screenshots
<img width="1366" height="768" alt="review1 png" src="https://github.com/user-attachments/assets/64ba2066-b5de-4763-addd-f05fbbd75f81" />
