# Networking Glossary

A running list of key terms from the Networking Bootcamp.  
Each entry includes a short definition, optional links and learning notes.

---

## Term: Networking

- **Definition**:  
  Your one-liner explanation.

- **Why it matters**:  
  (Optional) What problem it solves or why it's important.

- **AWS context**:  
  Where it shows up in AWS, if relevant.

- **Link**:  
  [Link to AWS docs]()

- **Personal Notes**:  
  Anything you misremember, how it clicked, or what to watch out for.

---

## Term: Subnet

- **Definition**:  
  Your one-liner explanation.

- **Why it matters**:  
  (Optional) What problem it solves or why it's important.

- **AWS context**:  
  Where it shows up in AWS, if relevant.

- **Link**:  
  [Link to AWS docs]()

- **Personal Notes**:  
  Anything you misremember, how it clicked, or what to watch out for.

---

## Term: Host

- **Definition**:  
  Your one-liner explanation.

- **Why it matters**:  
  (Optional) What problem it solves or why it's important.

- **AWS context**:  
  Where it shows up in AWS, if relevant.

- **Link**:  
  [Link to AWS docs]()

- **Personal Notes**:  
  Anything you misremember, how it clicked, or what to watch out for.

---

## Term: VLAN

- **Definition**:  
  Your one-liner explanation.

- **Why it matters**:  
  (Optional) What problem it solves or why it's important.

- **AWS context**:  
  Where it shows up in AWS, if relevant.

- **Link**:  
  [Link to AWS docs]()

- **Personal Notes**:  
  Anything you misremember, how it clicked, or what to watch out for.

---

## Term: VPC

- **Definition**:  
  Your one-liner explanation.

- **Why it matters**:  
  (Optional) What problem it solves or why it's important.

- **AWS context**:  
  Where it shows up in AWS, if relevant.

- **Link**:  
  [Link to AWS docs]()

- **Personal Notes**:  
  Anything you misremember, how it clicked, or what to watch out for.

---

## Term: Switches / Switching

- **Definition**:  
  Your one-liner explanation.

- **Why it matters**:  
  (Optional) What problem it solves or why it's important.

- **AWS context**:  
  Where it shows up in AWS, if relevant.

- **Link**:  
  [Link to AWS docs]()

- **Personal Notes**:  
  Anything you misremember, how it clicked, or what to watch out for.

---

## Term: Router / Routing

- **Definition**:  
  Your one-liner explanation.

- **Why it matters**:  
  (Optional) What problem it solves or why it's important.

- **AWS context**:  
  Where it shows up in AWS, if relevant.

- **Link**:  
  [Link to AWS docs]()

- **Personal Notes**:  
  Anything you misremember, how it clicked, or what to watch out for.

---

## Term: Route Table

- **Definition**:  
  Your one-liner explanation.

- **Why it matters**:  
  (Optional) What problem it solves or why it's important.

- **AWS context**:  
  Where it shows up in AWS, if relevant.

- **Link**:  
  [Link to AWS docs]()

- **Personal Notes**:  
  Anything you misremember, how it clicked, or what to watch out for.
  GenAI route tables?

---

## Term: Ethernet Frame

- **Definition**:  
  Your one-liner explanation.

- **Why it matters**:  
  (Optional) What problem it solves or why it's important.

- **AWS context**:  
  Where it shows up in AWS, if relevant.

- **Link**:  
  [Link to AWS docs]()

- **Personal Notes**:  
  🦉 Harry to Sirius: Ethernet Frame Edition

  🧙‍♂️ The Setup:

It’s late.
Harry’s in the Gryffindor common room.
He needs to send top-secret info to Sirius — but not over owl post (too obvious).
Instead, he uses a charms-enhanced tunnel of magic parchment running under Hogwarts — aka, the Ethernet cable.

But to send the letter through the tunnel, it has to be wrapped perfectly, or it won’t get delivered.

    The Ethernet Frame:

Your magical envelope.

1. Preamble
   Harry taps the parchment seven times with his wand.
   This wakes up the Hogwarts Underground Scroll Network and syncs it to receive incoming messages.
   Like whispering, “Oi, network, get ready!”

🪄 Magical handshake.

2. Destination MAC
   “To: Sirius Black (12 Grimmauld Place, Enchanted Firewall Alley, MAC #DEADBEEF)”
   The tunnel needs to know exactly which enchanted parchment to deliver to.
   Sirius’s home has a MAC address, just like every device on the network.

🕵️‍♂️ Targeted owl delivery, not a general howler.

3. Source MAC
   “From: Harry Potter (Gryffindor Tower, MAC #B00K5CAR)”
   Sirius needs to know who sent it.
   (Also helpful if he wants to send a reply with advice and mild panic.)

📨 Return address, magical style.

4. Type
   “Type: Order of the Phoenix Secret Message”
   This tells the tunnel what kind of scroll this is.
   Could be:

IPv4 spell (standard),

ARP scroll (who is this MAC?)

or something darker...

🧾 Tells Sirius how to decode the letter.

5. Data
   “They’re planning something. I saw Malfoy with Umbridge again.”
   This is the actual content Harry wants Sirius to read.
   Only a piece of a longer convo — more frames will follow.

📜 The heart of the message.

6. CRC (Cyclic Redundancy Check)
   Harry casts “Veritas Validatum” — a spell that checks if the parchment’s been tampered with.
   If even a single rune is off, Sirius’s receiver burns it.

🧪 Integrity check — no tampered scrolls allowed.

And the scroll flies down the enchanted Ethernet tunnel…
If it’s wrapped correctly? 📬 Sirius gets it.

If not? 🗑️ It vanishes into the network abyss, never reaching the fireplace.

| Frame Component     | Wizard Analogy                           | What It Actually Is                       |
| ------------------- | ---------------------------------------- | ----------------------------------------- |
| **Preamble**        | 7 wand taps to wake the tunnel           | Sync bits so the network starts listening |
| **Destination MAC** | “To: Sirius Black @ Grimmauld Place”     | Target device’s MAC address               |
| **Source MAC**      | “From: Harry Potter @ Gryffindor Tower”  | Sender’s MAC address                      |
| **Type**            | “This is an Order of the Phoenix scroll” | Tells what kind of payload (e.g. IPv4)    |
| **Data**            | “Malfoy is up to something...”           | Actual message/data inside the frame      |
| **CRC**             | Veritas Validatum spell                  | Error-checking code for integrity         |

---

## Term: IP Address - IPv4 and IPv6

- **Definition**:  
  Your one-liner explanation.

- **Why it matters**:  
  (Optional) What problem it solves or why it's important.

- **AWS context**:  
  Where it shows up in AWS, if relevant.

- **Link**:  
  [Link to AWS docs]()

- **Personal Notes**:  
  Anything you misremember, how it clicked, or what to watch out for.

---

## Term: Binary Math - Bit and Byte

- **Definition**:  
  Your one-liner explanation.

- **Why it matters**:  
  (Optional) What problem it solves or why it's important.

- **AWS context**:  
  Where it shows up in AWS, if relevant.

- **Link**:  
  [Link to AWS docs]()

- **Personal Notes**:

  🧳✨ Bits & Bytes as:
  **Mad-Eye Moody’s 7-Layer Magical Trunk**

🔹 The Trunk = Storage
Each compartment in the trunk = one bit.

So...

- 1 compartment = 1 bit = holds one thing (e.g., yes/no, true/false)
- 8 compartments stacked = 1 byte = now you can store something complex (like a face, or a full name)

Moody used it to hide:

- robes
- invisibility cloak
- a broom
- a full-grown human being - his real self

Just like:

- bytes store characters, numbers, pixels, spells
- more bytes = more detail, bigger secrets

  🧠 Why Not Logarithmic?

Because Moody’s trunk doesn’t shrink and expand by powers of 10.
It grows one creepy compartment at a time. You build it linearly.

But…

The number of things you can HIDE inside?
That grows exponentially with the number of compartments.

🧵 TL;DR:

- Bit = 1 compartment
- Byte = 8 compartments = 1 full room in Moody's trunk
- Add more bits? More compartments, more secrets.
- Logarithmic? Nah. It’s a dungeon, not a telescope.

---

## Term: Subnet Masks

- **Definition**:  
  Your one-liner explanation.

- **Why it matters**:  
  (Optional) What problem it solves or why it's important.

- **AWS context**:  
  Where it shows up in AWS, if relevant.

- **Link**:  
  [Link to AWS docs]()

- **Personal Notes**:  
  Anything you misremember, how it clicked, or what to watch out for.

---

## Term: Global Networks

- **Definition**:  
  Your one-liner explanation.

- **Why it matters**:  
  Backbone of X CSP.

- **AWS context**:  
  Where it shows up in AWS, if relevant.

- **Link**:  
  [Link to AWS docs]()

- **Personal Notes**:  
  Anything you misremember, how it clicked, or what to watch out for.

---

## Term: Global Infrastructure - Regions, Availability Zones,

- **Definition**:  
  Your one-liner explanation.

- **Why it matters**:  
  (Optional) What problem it solves or why it's important.

- **AWS context**:  
  Where it shows up in AWS, if relevant.

- **Link**:  
  [Link to AWS docs]()

- **Personal Notes**:  
  Anything you misremember, how it clicked, or what to watch out for.

---

## Term: Fault Tolerance - Fault Domain, Fault Level

- **Definition**:  
  Your one-liner explanation.

- **Why it matters**:  
  (Optional) What problem it solves or why it's important.

- **AWS context**:  
  Where it shows up in AWS, if relevant.

- **Link**:  
  [Link to AWS docs]()

- **Personal Notes**:  
  Anything you misremember, how it clicked, or what to watch out for.

---

## Term: Point of Presence (PoP)

- **Definition**:  
  Your one-liner explanation.

- **Why it matters**:  
  (Optional) What problem it solves or why it's important.

- **AWS context**:  
  Where it shows up in AWS, if relevant.

- **Link**:  
  [Link to AWS docs]()

- **Personal Notes**:  
  Anything you misremember, how it clicked, or what to watch out for.

---

## Term: AWS Security Groups vs NACL

- **Definition**:  
  Your one-liner explanation.

- **Why it matters**:  
  (Optional) What problem it solves or why it's important.

- **AWS context**:  
  Where it shows up in AWS, if relevant.

- **Link**:  
  [Link to AWS docs]()

- **Personal Notes**:  
  Anything you misremember, how it clicked, or what to watch out for.

---

## Term: Route 53

- **Definition**:  
  Your one-liner explanation.

- **Why it matters**:  
  (Optional) What problem it solves or why it's important.

- **AWS context**:  
  Where it shows up in AWS, if relevant.

- **Link**:  
  [Link to AWS docs]()

- **Personal Notes**:  
  Anything you misremember, how it clicked, or what to watch out for.

---

## Term: Azure Virtual Network (vNet) and Subnets

- **Definition**:  
  Your one-liner explanation.

- **Why it matters**:  
  (Optional) What problem it solves or why it's important.

- **AWS context**:  
  Where it shows up in AWS, if relevant.

- **Link**:  
  [Link to AWS docs]()

- **Personal Notes**:  
  Anything you misremember, how it clicked, or what to watch out for.

---

## Term: Network Security Groups

- **Definition**:  
  Your one-liner explanation.

- **Why it matters**:  
  (Optional) What problem it solves or why it's important.

- **AWS context**:  
  Where it shows up in AWS, if relevant.

- **Link**:  
  [Link to AWS docs]()

- **Personal Notes**:  
  Anything you misremember, how it clicked, or what to watch out for.

---

## Term: GCP Firewall Rules

- **Definition**:  
  Your one-liner explanation.

- **Why it matters**:  
  (Optional) What problem it solves or why it's important.

- **AWS context**:  
  Where it shows up in AWS, if relevant.

- **Link**:  
  [Link to AWS docs]()

- **Personal Notes**:  
  Anything you misremember, how it clicked, or what to watch out for.

---

## Term: [Term Name]

- **Definition**:  
  Your one-liner explanation.

- **Why it matters**:  
  (Optional) What problem it solves or why it's important.

- **AWS context**:  
  Where it shows up in AWS, if relevant.

- **Link**:  
  [Link to AWS docs]()

- **Personal Notes**:  
  Anything you misremember, how it clicked, or what to watch out for.

---

## Term: CIDR

- **Definition**:  
  Your one-liner explanation.

- **Why it matters**:  
  (Optional) What problem it solves or why it's important.

- **AWS context**:  
  Where it shows up in AWS, if relevant.

- **Link**:  
  [Link to AWS docs]()

- **Personal Notes**:  
  Anything you misremember, how it clicked, or what to watch out for.

---

## Term: Classful Addressing (deprecated by CIDR)

- **Definition**:  
  Your one-liner explanation.

- **Why it matters**:  
  (Optional) What problem it solves or why it's important.

- **AWS context**:  
  Where it shows up in AWS, if relevant.

- **Link**:  
  [Link to AWS docs]()

- **Personal Notes**:  
  Anything you misremember, how it clicked, or what to watch out for.

---

## Term: Classful Addressing (deprecated by CIDR)

- **Definition**:  
  Your one-liner explanation.

- **Why it matters**:  
  (Optional) What problem it solves or why it's important.

- **AWS context**:  
  Where it shows up in AWS, if relevant.

- **Link**:  
  [Link to AWS docs]()

- **Personal Notes**:  
  Anything you misremember, how it clicked, or what to watch out for.

---

## Term: Network Address Translation(NAT)

- **Definition**:  
  Your one-liner explanation.

- **Why it matters**:  
  (Optional) What problem it solves or why it's important.

- **AWS context**:  
  Where it shows up in AWS, if relevant.

- **Link**:  
  [Link to AWS docs]()

- **Personal Notes**:  
  Anything you misremember, how it clicked, or what to watch out for.

---

## Term: [Term Here]

- **Definition**:  
  Your one-liner explanation.

- **Why it matters**:  
  (Optional) What problem it solves or why it's important.

- **AWS context**:  
  Where it shows up in AWS, if relevant.

- **Link**:  
  [Link to AWS docs]()

- **Personal Notes**:  
  Anything you misremember, how it clicked, or what to watch out for.

---

## Term: [Term Here]

- **Definition**:  
  Your one-liner explanation.

- **Why it matters**:  
  (Optional) What problem it solves or why it's important.

- **AWS context**:  
  Where it shows up in AWS, if relevant.

- **Link**:  
  [Link to AWS docs]()

- **Personal Notes**:  
  Anything you misremember, how it clicked, or what to watch out for.

---

## Term: [Term Here]

- **Definition**:  
  Your one-liner explanation.

- **Why it matters**:  
  (Optional) What problem it solves or why it's important.

- **AWS context**:  
  Where it shows up in AWS, if relevant.

- **Link**:  
  [Link to AWS docs]()

- **Personal Notes**:  
  Anything you misremember, how it clicked, or what to watch out for.

---

## Term: [Term Here]

- **Definition**:  
  Your one-liner explanation.

- **Why it matters**:  
  (Optional) What problem it solves or why it's important.

- **AWS context**:  
  Where it shows up in AWS, if relevant.

- **Link**:  
  [Link to AWS docs]()

- **Personal Notes**:  
  Anything you misremember, how it clicked, or what to watch out for.

---

## Term: [Term Here]

- **Definition**:  
  Your one-liner explanation.

- **Why it matters**:  
  (Optional) What problem it solves or why it's important.

- **AWS context**:  
  Where it shows up in AWS, if relevant.

- **Link**:  
  [Link to AWS docs]()

- **Personal Notes**:  
  Anything you misremember, how it clicked, or what to watch out for.

---

## Term: [Term Here]

- **Definition**:  
  Your one-liner explanation.

- **Why it matters**:  
  (Optional) What problem it solves or why it's important.

- **AWS context**:  
  Where it shows up in AWS, if relevant.

- **Link**:  
  [Link to AWS docs]()

- **Personal Notes**:  
  Anything you misremember, how it clicked, or what to watch out for.

---

## Term: [Term Here]

- **Definition**:  
  Your one-liner explanation.

- **Why it matters**:  
  (Optional) What problem it solves or why it's important.

- **AWS context**:  
  Where it shows up in AWS, if relevant.

- **Link**:  
  [Link to AWS docs]()

- **Personal Notes**:  
  Anything you misremember, how it clicked, or what to watch out for.

---

## Term: [Term Here]

- **Definition**:  
  Your one-liner explanation.

- **Why it matters**:  
  (Optional) What problem it solves or why it's important.

- **AWS context**:  
  Where it shows up in AWS, if relevant.

- **Link**:  
  [Link to AWS docs]()

- **Personal Notes**:  
  Anything you misremember, how it clicked, or what to watch out for.

---

## Term: [Term Here]

- **Definition**:  
  Your one-liner explanation.

- **Why it matters**:  
  (Optional) What problem it solves or why it's important.

- **AWS context**:  
  Where it shows up in AWS, if relevant.

- **Link**:  
  [Link to AWS docs]()

- **Personal Notes**:  
  Anything you misremember, how it clicked, or what to watch out for.

---

## Term: [Term Here]

- **Definition**:  
  Your one-liner explanation.

- **Why it matters**:  
  (Optional) What problem it solves or why it's important.

- **AWS context**:  
  Where it shows up in AWS, if relevant.

- **Link**:  
  [Link to AWS docs]()

- **Personal Notes**:  
  Anything you misremember, how it clicked, or what to watch out for.

---

## Term: [Term Here]

- **Definition**:  
  Your one-liner explanation.

- **Why it matters**:  
  (Optional) What problem it solves or why it's important.

- **AWS context**:  
  Where it shows up in AWS, if relevant.

- **Link**:  
  [Link to AWS docs]()

- **Personal Notes**:  
  Anything you misremember, how it clicked, or what to watch out for.

---

## Term: [Term Here]

- **Definition**:  
  Your one-liner explanation.

- **Why it matters**:  
  (Optional) What problem it solves or why it's important.

- **AWS context**:  
  Where it shows up in AWS, if relevant.

- **Link**:  
  [Link to AWS docs]()

- **Personal Notes**:  
  Anything you misremember, how it clicked, or what to watch out for.

---

## Term: [Term Here]

- **Definition**:  
  Your one-liner explanation.

- **Why it matters**:  
  (Optional) What problem it solves or why it's important.

- **AWS context**:  
  Where it shows up in AWS, if relevant.

- **Link**:  
  [Link to AWS docs]()

- **Personal Notes**:  
  Anything you misremember, how it clicked, or what to watch out for.

---

## Term: [Term Here]

- **Definition**:  
  Your one-liner explanation.

- **Why it matters**:  
  (Optional) What problem it solves or why it's important.

- **AWS context**:  
  Where it shows up in AWS, if relevant.

- **Link**:  
  [Link to AWS docs]()

- **Personal Notes**:  
  Anything you misremember, how it clicked, or what to watch out for.

---

## Term: [Term Here]

- **Definition**:  
  Your one-liner explanation.

- **Why it matters**:  
  (Optional) What problem it solves or why it's important.

- **AWS context**:  
  Where it shows up in AWS, if relevant.

- **Link**:  
  [Link to AWS docs]()

- **Personal Notes**:  
  Anything you misremember, how it clicked, or what to watch out for.

---
