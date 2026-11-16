# Database security audit & remediation

**55 production tables moved from blanket access to scoped access, with zero downtime.**

![Tables](https://img.shields.io/badge/tables%20secured-55-2ea043)
![Downtime](https://img.shields.io/badge/downtime-zero-635bff)
![Migrations](https://img.shields.io/badge/migrations-3-f78166)

- Audited a live production schema holding payroll and guest data
- Shipped mid-service in four stages, with nobody locked out
- Remaining risks written up, not hidden

> Source is private (live business system). **[Full write-up →](https://sajjad.omni-genai.com/projects/database-security)**

`PostgreSQL` · `Supabase` · `Row-level security` · `SQL migrations` · `SECURITY DEFINER`

<details>
<summary><b>How it shipped without downtime</b></summary>

```mermaid
flowchart LR
    A[1 · Add scoped<br/>policies] --> B[2 · App release<br/>with signed-in access]
    B --> C[3 · Confirm every<br/>device updated]
    C --> D[4 · Remove old<br/>open policies]
```

Each stage was safe on its own, so the system stayed up the whole time.

</details>

<details>
<summary><b>What I delivered</b></summary>

- A full audit of 55 production tables.
- Three migrations covering payroll, operations and rota, and financial, stock and document tables.
- Access rules built on SECURITY DEFINER helper functions.
- A written record of the remaining risks, so the next piece of work starts from a true picture.

</details>

---

Built by **[Sajjad Mahessar](https://sajjad.omni-genai.com)** · [LinkedIn](https://www.linkedin.com/in/sajjadmahessar/)
