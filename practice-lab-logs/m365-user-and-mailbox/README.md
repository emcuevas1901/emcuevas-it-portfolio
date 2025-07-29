## 🧠 Microsoft 365 & Entra ID Lab Overview

Denne seksjonen simulerer virkelige onboarding- og identitetshåndteringsoppgaver som vanligvis utføres av IT-supportteknikere. Tabellen under oppsummerer hvert steg og hvilke verktøy som ble brukt gjennom hele laben.

### 🧪 Oppgaver og Verktøy

| Steg | Oppgave | Verktøy |
| --- | --- | --- |
| 1 | Opprett en ny bruker | Microsoft 365 Admin Center |
| 2 | Tildel Microsoft 365 E5 Developer-lisens | Microsoft 365 Admin Center |
| 🔐 (Ekstra) | Aktiver MFA for John IT | Microsoft 365 Admin Center |
| 3 | Opprett sikkerhetsgruppe | Entra ID (entra.microsoft.com) |
| 4 | Legg til John IT i sikkerhetsgruppen | Entra ID |
| 5 | Opprett delt postboks (f.eks. support@...) | Microsoft 365 Admin Center |
| 6 | **Tildel tilgang** til John IT for postboksen | Microsoft 365 Admin Center |
| ✅ (Valgfritt) | Tildel en innebygd Entra-rolle (f.eks. Group Admin) | Entra ID |
| ✅ (Valgfritt) | Åpne delt postboks via Outlook Web  | outlook.office.com |

### 🧑‍💻 Steg 1 – Opprett en ny bruker

**📝 Beskrivelse:**

Opprettet en bruker med navnet **John IT** via Microsoft 365 Admin Center for å simulere onboarding av en ny ansatt i en bedriftskontekst.

---

**✅ Utførte handlinger:**

- Gikk til admin.microsoft.com
- Navigerte til **Brukere → Aktive brukere**
- Klikket **Legg til en bruker**
- Fylte inn:
    - Visningsnavn: `John IT`
    - Brukernavn: `john.it@yourdomain.onmicrosoft.com`
- Satte et tilpasset passord
- Aktiverte **"Krev passordendring ved første pålogging"**
- Lagret brukeren

---

**📸 Screenshot:**

![Microsoft 365 add user.png](attachment:a3584c5b-4c95-45cb-b2bb-c678325156b7:Microsoft_365_add_user.png)

![microsoft 365 add user created.png](attachment:815f7204-cdb0-4432-8033-bc6f85b00fe4:microsoft_365_add_user_created.png)

---

### 💳 Steg 2 – Tildel Microsoft 365-lisens

**📝 Beskrivelse:**

Tildelte lisensen **Microsoft 365 E5 Developer** til `John IT` for å aktivere tilgang til Exchange Online, OneDrive, SharePoint og andre sentrale Microsoft 365-tjenester.

---

**✅ Utførte handlinger:**

- Fortsatt inne i admin.microsoft.com
- Klikket på `John IT` fra listen over aktive brukere
- Åpnet fanen **Lisenser og apper**
- Huket av for **Microsoft 365 E5 Developer**
- Lot alle standardapper være aktivert
- Klikket **Lagre endringer**

![microsoft 365 add user created.png](attachment:b67dc513-ca44-445d-b03b-5213aaaf838b:microsoft_365_add_user_created.png)

### 🔐 Valgfritt steg – Aktiver MFA for John IT

**📝 Beskrivelse:**

Aktiverte Multi-Factor Authentication (MFA) for brukeren `John IT` for å simulere sikre påloggingsrutiner i Microsoft 365-miljøer.

---

**✅ Utførte handlinger:**

- Logget inn på admin.microsoft.com
- Gikk til **Brukere → Aktive brukere**
- Klikket på **“Multi-factor authentication”** i toppmenyen
- Valgte `John IT` fra listen
- Klikket **Aktiver**, og bekreftet valget

---

**📘 Notater:**

- Nåværende MFA-status: **Aktivert**
- Status endres automatisk til **Påkrevd** når `John IT` fullfører oppsettet (f.eks. via Authenticator-app eller SMS-bekreftelse ved innlogging)

---

**📸 Skjermbilde:**

Administrasjonssiden for MFA som viser at `John IT` har status **“Enabled”**, noe som betyr at MFA kreves ved neste innlogging.

![enabling mfa.png](attachment:9e826383-4e78-41e7-ad72-6f9829bd0420:enabling_mfa.png)

---

**💡 Hvorfor dette er viktig:**

I de fleste moderne IT-miljøer er MFA et grunnleggende sikkerhetskrav. Denne oppgaven viser at du har forståelse for identitetsbeskyttelse og sikring av brukerkontoer — vanlige ansvarsområder i en IT-supportrolle.

---

### 👥 Steg 3 – Opprett sikkerhetsgruppe i Entra ID

**📝 Beskrivelse:**

Opprettet en **sikkerhetsgruppe** i Microsoft Entra Admin Center (tidligere Azure AD) for å simulere rollebasert tilgangsstyring for IT-supportbrukere.

---

**✅ Utførte handlinger:**

- Logget inn på [https://entra.microsoft.com](https://entra.microsoft.com/)
- Navigerte til **Grupper → Alle grupper**
- Klikket på **“+ Ny gruppe”**
- Fylte inn:
    - **Gruppetype:** Sikkerhet
    - **Gruppenavn:** Support Team
    - **Beskrivelse:** Helpdesk og supportbrukere
    - **Medlemstype:** Tildelt
- La til medlem: `John IT`
- Klikket **Opprett**

---

**📸 Skjermbilde:**

Detaljsiden for gruppen viser at “Support Team” er opprettet med `John IT` som medlem.

![new group + add .png](attachment:e1a86cc2-0b01-47ad-8939-75fb589cd802:new_group__add_.png)

![new group + add 2.png](attachment:28dae018-a08f-40e4-ae74-83c1fb6019e3:new_group__add_2.png)

---

**💡 Hvorfor dette er viktig:**

Sikkerhetsgrupper gjør det mulig å tildele like rettigheter på tvers av tjenester som SharePoint, Exchange og Intune. I IT-supportroller er det avgjørende å kunne opprette og administrere grupper for å sikre skalerbar tilgangskontroll.

---

### 📧 Steg 4 – Opprett delt postboks og tildel tilgang

**📝 Beskrivelse:**

Opprettet en delt postboks og tildelte tilgang til `John IT`, for å simulere en vanlig IT-supportoppgave hvor en ansatt skal lese og sende e-post fra en fellesadresse.

---

**✅ Utførte handlinger:**

- Logget inn på admin.microsoft.com
- Gikk til **Teams og grupper → Delte postbokser**
- Klikket **+ Legg til delt postboks**
- Fylte inn:
    - Navn: `Support Mailbox`
    - E-postadresse: `support@yourdomain.onmicrosoft.com`
- Klikket **Lagre**
- Åpnet den nye postboksen → Klikket **Rediger medlemmer**
- La til `John IT` som medlem

---

**📸 Skjermbilde:**

Delt postboks som viser `support@...` med `John IT` oppført som medlem med full tilgang.

![delte postboks.png](attachment:0431b7af-b5b8-4403-8e3c-486fde0c7d8e:delte_postboks.png)

---

**💡 Hvorfor dette er viktig:**

Delte postbokser brukes av team (f.eks. helpdesk eller HR) til å håndtere felles kommunikasjon. Å tildele tilgang til slike postbokser er en vanlig oppgave for IT-supportpersonell i førstelinje.

---

### 📧 Steg 6 – Tildel tilgang til delt postboks

**📝 Beskrivelse:**

Tildelte `John IT` både **Send som**- og **Full tilgang**-rettigheter til postboksen `support@...`, for å simulere delte team-innbokser i en IT-supportsituasjon.

---

**✅ Utførte handlinger:**

- Gikk til [admin.microsoft.com](https://admin.microsoft.com/)
- Navigerte til **Teams og grupper → Delte postbokser**
- Valgte `Support Mailbox`
- Under **Send som**:
    - Klikket **Rediger → + Legg til personer → John IT**
- Under **Full tilgang**:
    - Klikket **Rediger → + Legg til personer → John IT**

---

**📸 Skjermbilde:**

Vist tilgangsfanene for "Send som" og "Full tilgang", med `John IT` lagt til

![delte postboks tillatelser 1.png](attachment:e4b5ba4c-4638-4370-a6d5-3f14282f7c09:delte_postboks_tillatelser_1.png)

![delte postboks tillatelser 2.png](attachment:d4b701cb-53eb-42e5-8685-b8c61077c13e:delte_postboks_tillatelser_2.png)

---

**💡 Hvorfor dette er viktig:**

Delt tilgang til en innboks gjør det mulig for teammedlemmer å svare på henvendelser fra en fellesadresse – noe som er vanlig i helpdesk- og supportmiljøer.

---

### 👤 Ekstra Steg – Tilordne innebygd Entra-rolle

**📝 Beskrivelse:**

Tildelte `John IT` rollen **Groups Administrator** i Entra ID for å simulere rollebasert tilgangskontroll i Microsoft 365-miljøer.

---

**✅ Utførte handlinger:**

- Gikk til [entra.microsoft.com](https://entra.microsoft.com/)
- Åpnet **Users → John IT**
- Gikk til fanen **Assigned roles**
- Klikket **+ Add assignments**
- Valgte `Groups Administrator`
- Bekreftet og lagret endringen

---

**📸 Skjermbilde:**

Viser tildelt rolle under `John IT → Assigned Roles`

![assign entra id role.png](attachment:74760b03-5619-4ea1-97d0-c7ac7f449975:assign_entra_id_role.png)

---

**💡 Hvorfor dette er viktig:**

Rollebasert tilgang (RBAC) gjør det mulig å gi ansatte tilgang til nøyaktig det de trenger – og ingenting mer. Dette er en viktig del av sikker og effektiv brukeradministrasjon.

---

### ✅ Ekstra Steg – Åpne delt postboks i Outlook Web

**📝 Beskrivelse:**

Logget inn som `John IT` i Outlook Web for å bekrefte at han hadde tilgang til den delte postboksen `support@...`, og kunne sende e-post som denne adressen.

---

**✅ Utførte handlinger:**

- Gikk til [outlook.office.com](https://outlook.office.com/)
- Logget inn som `john.it@...`
- Åpnet venstre panel og fant `Support Mailbox`
- Sendte en testmail med **"Fra"** satt til `support@...`

---

**📸 Skjermbilde:**

Viser `Support Mailbox` i sidepanel, eller e-post sendt som `support@...`

![outlook oline.png](attachment:d646027d-c961-436e-a691-1c7d5286572b:outlook_oline.png)

![outlook app.png](attachment:a93a2c4e-e3f0-41a6-a100-6e1d66e1213f:outlook_app.png)

---

**💡 Hvorfor dette er viktig:**

Bekrefter at tillatelsene er brukt riktig i praksis. Å teste i sluttbrukergrensesnittet (Outlook Web) er en vanlig oppgave i IT-support.
