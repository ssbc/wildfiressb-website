---
title: WildfireSSB
permalink: /index.html
description: 'Eleventy Excellent is inspired bythe companion website of Andy Bell’s talk "Be the browser’s mentor, not its micromanager".'
layout: index
---

<div class="wrapper">
  <header class="full | section" style="--spot-color: var(--color-primary)">
    <div class="section__inner flow region">
      <h1 class="text-center text-base-light">{{ title }}</h1>
    </div>

    {% svg "divider/waves", null, "seperator" %}
  </header>

## Problem Statement
Wildfires are a growing global threat, intensified by climate change. South America, in particular, faces increasing risks, as many regions suffer from devastating fires year after year. Effective communication among firefighters and emergency responders is critical to managing and mitigating the impact of these wildfires. However, communication systems in remote areas often fail due to damaged infrastructure, lack of cellular coverage, or overwhelmed networks.

In these critical moments, the lack of reliable communication can lead to delayed responses, poor coordination, and increased danger to both responders and civilians. Without effective coordination, resources are stretched thin, and decision-making becomes chaotic, worsening the situation.

## What We Seek to Do
At WildfireSSB, our mission is to empower firefighters and first responders in South America with decentralized, resilient communication tools that work even in the absence of traditional infrastructure. We aim to equip emergency teams with the ability to communicate and coordinate effectively, no matter the circumstances. 

To solve this, we are leveraging two key open-source technologies:

1. TinySSB (Secure ScuttleButt): A peer-to-peer communication protocol that allows devices to sync and share critical data without needing a centralized server or internet connection.
2. ATAK (Android Team Awareness Kit): A situational awareness platform already used by U.S. firefighters to map fire perimeters, share real-time data, and coordinate team movements.

Our goal is to adapt these technologies to the specific needs of firefighters in South America, enabling peer-to-peer communication, secure data sharing, and real-time situational awareness in even the most remote or fire-affected areas.

## Technologies Involved
### TinySSB (Secure ScuttleButt)

![tinySSB banner](/assets/images/gallery/tinySSB-banner.png)

TinySSB is a decentralized protocol that enables users to share data and messages without needing an internet connection or centralized server. It is designed to work in low-bandwidth environments, making it ideal for use in remote areas or during network failures.

- Peer-to-peer: Devices communicate directly with each other over whatever means are available (bluetooth, wifi, lora), reducing reliance on external infrastructure.

** falta imagen LoRa**

- Data synchronization: Teams can share maps, task lists, and critical updates, ensuring that everyone has access to the most up-to-date information, even offline.

![TAK](/assets/images/gallery/cropped-TAK-CIV-Splash-4.png)

## ATAK (Android Team Awareness Kit)
ATAK is a powerful situational awareness tool that helps emergency teams track resources, coordinate movements, and visualize the area in real time. Initially developed for military and first responders, it has been proven effective in wildfire response.

- Real-time mapping: Teams can view fire perimeters, terrain, and responder locations on shared maps.

** falta imagen ATAC**

- Coordination: Responders can exchange messages, share geolocated data, and track resources to optimize their efforts.

By combining TinySSB’s decentralized communication with ATAK’s situational awareness capabilities, we are building a resilient system tailored to firefighting and emergency response.

## Architecture Description
Our solution is based on device-to-device (D2D) communication using TinySSB, where each firefighter or responder is equipped with a smartphone or tablet running both TinySSB and ATAK. Here’s how it works:

1. Peer-to-peer network: In the field, devices create a mesh network through TinySSB, allowing direct communication between nearby responders. No internet or cellular network is needed.
2. Situational awareness with ATAK: Responders use ATAK to visualize the environment, track fire perimeters, and share real-time data (such as locations and status updates) with their peers.
3. Offline-first design: Even if all external networks fail, responders can still exchange critical information and maintain an updated view of the situation.
4. Efficient synchronization: Once a device connects to a central hub or network (such as when entering a connected area), all data gathered during the mission is synchronized and shared.

This distributed architecture ensures that teams can continue their work uninterrupted, even in challenging, fire-affected environments where communication infrastructure has been compromised.

## What Is Our Next Step
We are currently developing and testing our system with local firefighting teams in Argentina. Our immediate next step is to:

1 Launch a pilot project: We plan to deploy this system with local fire departments to gather real-world feedback, refine the tools, and demonstrate their effectiveness in combating wildfires.
2 Expand community involvement: working with open-source contributors, designers, and local communities to create educational materials, develop additional features, and ensure widespread adoption.
3 Secure funding: Donations made through Gitcoin will allow us to:
  - Continue development and testing.
  - Train local responders on how to use TinySSB and ATAK effectively.
  - Scale the system to more regions.

  ## Partners
Our project is a joint effort between a wide range of organizations and communities, each bringing unique expertise and local knowledge to help us tackle the wildfire communication challenge:

- SecureScuttleButt (SSB) Community: The SSB community is a vibrant group of developers and decentralization advocates who have contributed to the development of TinySSB. Their expertise in peer-to-peer technologies has been foundational in building resilient, offline-first communication tools.

- Programa para contingencias ante desastres naturales y mitigar los efectos del cambio climático en el paraje Las Lagunitas. This Argentinian proyect by University of Río Cuarto width a team  is playing a vital role in connecting us with local firefighters and conducting field research.

- Comunidad de Alpa Corral: A small community in the Sierras de Córdoba, Alpa Corral has been directly affected by wildfires. The local community is providing crucial feedback on the development of tools that suit the on-ground realities of firefighting in rural areas.

- Ahau.io (Maori Nation): Ahau.io is a decentralized information system created by the Māori Nation in New Zealand. Their commitment to preserving indigenous knowledge through technology mirrors our goal of empowering local communities with open-source tools. They serve as a model for how decentralized technologies can protect and share local knowledge.

## Prior Art
We stand on the shoulders of pioneers who have been experimenting with decentralized communication technologies in remote and challenging environments:

- Christian F Tschudin, Mix Irving, and Nanomonkey's work with TinySSB: These three core contributors to the SecureScuttleButt ecosystem have been instrumental in developing TinySSB, a lightweight version of SSB designed for low-bandwidth, intermittent connections. Their work is the backbone of WildfireSSB.

- Luandro’s experiments with Meshtastic in the Amazon: Luandro has been testing the use of Meshtastic, a low-power, long-range communication protocol, in the remote Amazon region. His experiments offer invaluable insights into how decentralized communication can function in areas with little to no infrastructure:

![map Meshtastic](/assets/images/gallery/mapa_meshtastic.jpeg)
https://meshtastic.discourse.group/t/meshtastic-to-connect-remote-villages-deep-in-the-amazon/2643/1

- Nico Pace’s Meshtastic trials in the hills of Córdoba and with Luandro for Communities in the Amazon: Nico has been experimenting with Meshtastic to build reliable communication systems for firefighters and forest rangers in Argentina’s remote and wildfire-prone regions. His real-world testing helps inform our approach to integrating these tools with ATAK.

**falta imagen**
https://nico.today/tracking-canoes-with-meshtastic/

## Who's involved
Our team is composed of individuals with deep expertise in decentralized technology, open-source development, and on-the-ground firefighting:

- Christian F Tschudin: Core contributor to the TinySSB protocol and SecureScuttleButt community, Cft brings expertise in peer-to-peer networking and decentralized systems. Professor at …
- Mix Irving: Developer working on TinySSB, SecureScuttleButt and Ahau, and other decentralized technologies. Mix’s technical skills ensure that the tools we build are both robust and scalable for real-world use.
- Nico Pace: Project leader and experimenter in decentralized technologies for firefighting and remote area communication. Nico’s fieldwork in Córdoba, Argentina, is crucial to tailoring these tools to the needs of firefighters.
- Luandro Viera: Researcher and developer who has been experimenting with Meshtastic in the Amazon. His insights on real-world deployments are invaluable to our mission.
- Nanomonkey: Contributor to SecureScuttleButt and TinySSB, focused on lightweight, offline-first solutions.

## Marketing
We've developed a range of marketing assets to help spread the word about WildfireSSB and its mission to improve wildfire response in remote regions through open-source technology.

In this google drive you will find our marketing assets to download:

- Social media graphics (for Twitter, Instagram, and Facebook)
- Videos showcasing how the technology works
- Infographics explaining decentralized communication for firefighters

Feel free to share these materials and help us get more people involved in supporting this important cause!

## How You Can Contribute
We need your support to make this project a reality! Here's how you can get involved:

- Donate through Gitcoin: Your contributions will directly support the development, testing, and deployment of these lifesaving tools. Plus, your donations will be matched by Gitcoin’s grant round, making every contribution even more impactful.
- Contribute to the code: If you're a developer, join our community and help us build robust, open-source tools for wildfire response.
- Spread the word: Share our project on social media, tell your friends, or write a blog post. Every bit of awareness helps.
- Design and community engagement: Help us create educational resources, training materials, or work on UI/UX design to make the system easy to use.

Together, we can make a real difference in the fight against wildfires, protecting both people and the environment.

Join us in building a resilient future for wildfire response! #gg22 #wildfire #tech #oss #p2p #ATAK
