# Architectural Requirements

This is a living document with the architectural requirements of the **User Management Dashboard with QR-Based vCard Sharing**.

For more information, check out the [Project Spec](./project-spec.md).

---

## Constraints

| Constraint                                                       | Context                                                                                                      |
| ---------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------ |
| [Technical] Must use **React** (frontend) and **Node.js + MongoDB** (backend) | The current development team has expertise in React and Node.js; MongoDB was chosen for flexibility.         |
| [Technical] Must be responsive and functional on tablets & desktop | Admins primarily use laptops or tablets to manage employees.                                                 |
| [Business] Must ship MVP within 1 month                           | The digital business card feature is required for an upcoming company networking event.                       |
| [Technical] QR codes and vCards must be generated in the backend  | Ensures security and consistent data handling across all clients.                                            |

---

## Quality Attributes

| Quality Attribute | Scenario                                                                                       | Priority |
| ----------------- | ---------------------------------------------------------------------------------------------- | -------- |
| Usability         | An admin with no technical background can create and share an employee profile in under 2 mins | High     |
| Security          | Only authenticated admins can access or modify employee records                                 | High     |
| Compatibility     | vCard files should import seamlessly into iOS, Android, and desktop contact managers            | High     |
| Performance       | QR code generation and vCard download should complete in less than 3 seconds                    | Medium   |
| Scalability       | The system should be able to handle 10,000+ employee records without performance degradation    | Medium   |
| Deployability     | Code changes should be deployable to production within 30 minutes                               | Low      |

---

## Influential Functional Requirements

- Admins can create, edit, and delete employee profiles with required and optional fields.
- The backend automatically generates and serves QR codes linking to downloadable vCard (.vcf) files.
- Admins can view or download QR codes directly from the dashboard.

---

## Other Influencers

- The current development team consists of **1 frontend React developers** and **1 backend Node.js developer**.
- All team members are familiar with **React** and **Tailwind CSS**; only one developer has advanced TypeScript experience (gradual adoption planned).
- No mobile app is planned; the MVP is strictly web-based.

