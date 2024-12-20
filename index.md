{:refdef: style="text-align: center;"}
![](img/Sk_fuQOxyl.png)
{: refdef}

# WildfireSSB: Decentralized Communication for Wildfire Response

<div style="text-align: center;">
  <a href="https://explorer.gitcoin.co/#/round/42161/608/115" class="button" style="display: inline-block; padding: 10px 20px; font-size: 16px; color: white; background-color: #007bff; text-decoration: none; border-radius: 5px;">Support us through a donation on Gitcoin</a>
</div>



Wildfires are a growing global threat, intensified by climate change. South America, in particular, faces increasing risks, as many regions suffer from devastating fires year after year. Effective communication among firefighters and emergency responders is critical to managing and mitigating the impact of these wildfires. However, communication systems in remote areas often fail due to damaged infrastructure, lack of cellular coverage, or overwhelmed networks.

In these critical moments, the lack of reliable communication can lead to delayed responses, poor coordination, and increased danger to both responders and civilians. Without effective coordination, resources are stretched thin, and decision-making becomes chaotic, worsening the situation.

## What We Seek to Do

**WildfireSSB** mission is to empower fire fighters and first responders in South America and beyond with **decentralized, resilient communication tools** that work even in the absence of traditional infrastructure. We aim to equip emergency teams with the ability to communicate and coordinate effectively, no matter the circumstances.

To solve this, we are leveraging two key open-source technologies:

1. **TinySSB (Secure ScuttleButt)**: A peer-to-peer communication protocol that allows devices to sync and share critical data without needing a centralized server or internet connection.
2. **ATAK (Android Team Awareness Kit)**: A mature situational awareness platform already used by U.S. firefighters to map fire perimeters, share real-time data, and coordinate team movements.

Our goal is to adapt these technologies to the specific needs of firefighters in South America, enabling **peer-to-peer communication, secure data sharing, and real-time situational awareness** in even the most remote or fire-affected areas.

## Technologies Involved

### TinySSB (Secure ScuttleButt)

![tinySSB banner](img/tinySSB-banner.png)

[TinySSB](https://github.com/ssbc/tinySSB) is a **decentralized protocol** that enables users to share data and messages without needing an internet connection or centralized server. It is designed to work in low-bandwidth environments, making it ideal for use in remote areas or during network failures.

- **Peer-to-peer**: Devices communicate directly with each other over whatever means are available (bluetooth, wifi, lora), reducing reliance on external infrastructure.

![LoRa banner](img/ryqfDXOl1l.jpg)

- **Data synchronization**: Teams can share maps, task lists, and critical updates, ensuring that everyone has access to the most up-to-date information, even offline.

![TAK](img/cropped-TAK-CIV-Splash-4.png)

### ATAK (Android Team Awareness Kit)
ATAK is a powerful **situational awareness** tool that helps emergency teams track resources, coordinate movements, and visualize the area in real time. Initially developed for military, it has been proven effective in **wildfire response**  and first responders.

- **Real-time mapping**: Teams can view fire perimeters, terrain, and responder locations on shared maps.

![mapa TAK](img/Hyf8IUJJke.png)

- **Coordination**: Responders can exchange messages, share geolocated data, and track resources to optimize their efforts.

By combining **TinySSB’s decentralized communication** with **ATAK’s situational awareness** capabilities, we are building a resilient system tailored to firefighting and emergency response.

## Architecture Description

Our approach is based on **device-to-device (D2D) communication** using TinySSB, where each firefighter or responder is equipped with a smartphone or tablet running both TinySSB and ATAK. Here’s how it works:

1. **Peer-to-peer network**: In the field, devices create a mesh network through TinySSB, allowing direct communication between nearby responders. No internet or cellular network is needed.
2. **Situational awareness with ATAK**: Responders use ATAK to visualize the environment, track fire perimeters, and share real-time data (such as locations and status updates) with their peers.
3. **Offline-first design**: Even if all external networks fail, responders can still exchange critical information and maintain an updated view of the situation.
4. **Efficient synchronization**: Once a device connects to a central hub or network (such as when entering a connected area), all data gathered during the mission is synchronized and shared.

This **distributed architecture** ensures that teams can continue their work uninterrupted, even in challenging, fire-affected environments where communication infrastructure has been compromised.

## What Is Our Next Step

We are currently designing the system with local firefighting teams in Argentina. Our immediate next step is to:

1. **Launch a pilot project**: We plan to deploy this system with local fire departments to gather real-world feedback, refine the tools, and demonstrate their effectiveness in combating wildfires.
2. **Expand community involvement**: working with open-source contributors, designers, and local communities to create educational materials, develop additional features, and ensure widespread adoption.
3. **Secure funding**: Donations made through Gitcoin will allow us to:
   - Continue development and testing.
   - Train local responders on how to use TinySSB and ATAK effectively.
   - Scale the system to more regions.

## Partners

Our project is a joint effort between a wide range of organizations and communities, each bringing unique expertise and local knowledge to help us tackle the wildfire communication challenge:

- **[SecureScuttleButt](https://scuttlebutt.nz/) (SSB) Community**: The SSB community is a vibrant group of developers and decentralization advocates who have contributed to the development of TinySSB. Their expertise in peer-to-peer technologies has been foundational in building resilient, offline-first communication tools.
  
- **Universidad de Río Cuarto**: This Argentinian university is playing a vital role in connecting us with local firefighters and conducting field research.
  
- **Comunidad de Alpa Corral**: A small community in the Sierras de Córdoba, Alpa Corral has been directly affected by wildfires. The local community is providing crucial feedback on the development of tools that suit the on-ground realities of firefighting in rural areas.
  
- **Ahau.io (Maori Nation)**: Ahau.io is a decentralized information system created by the Māori Nation in New Zealand. Their commitment to preserving indigenous knowledge through technology mirrors our goal of empowering local communities with open-source tools. They serve as a model for how decentralized technologies can protect and share local knowledge.

## Prior Art

We stand on the shoulders of pioneers who have been experimenting with decentralized communication technologies in remote and challenging environments:

- **[Christian F Tschudin](https://github.com/tschudin), [Mix Irving](https://github.com/mixmix), and [Nanomonkey](https://github.com/nanomonkey)'s work with TinySSB**: These three core contributors to the SecureScuttleButt ecosystem have been instrumental in developing TinySSB, a lightweight version of SSB designed for low-bandwidth, intermittent connections. Their work is the backbone of WildfireSSB.
  
- **[Luandro Viera](https://github.com/luandro/)’s experiments with Meshtastic in the Amazon**: Luandro has been testing the use of Meshtastic, a low-power, long-range communication protocol, in the remote Amazon region. His experiments offer invaluable insights into how decentralized communication can function in areas with little to no infrastructure:
 
![map Meshtastic](img/e6e5ab575cd6c6a743bdea44c844e7ad4cb6594c_2_690x298.jpeg)
https://meshtastic.discourse.group/t/meshtastic-to-connect-remote-villages-deep-in-the-amazon/2643/1

- **Nico Pace’s Meshtastic trials in the hills of Córdoba and with Luandro for Communities in the Amazon**: Nico has been experimenting with Meshtastic to build reliable communication systems for firefighters and forest rangers in Argentina’s remote and wildfire-prone regions. His real-world testing helps inform our approach to integrating these tools with ATAK.

![boats](img/r1LJsXOlJe.png)
https://nico.today/tracking-canoes-with-meshtastic/

## Who's involved

Our team is composed of individuals with deep expertise in decentralized technology, open-source development, and on-the-ground firefighting:

- **[Christian F Tschudin](https://github.com/tschudin)**: Core contributor to the TinySSB protocol and SecureScuttleButt community, Cft brings expertise in peer-to-peer networking and decentralized systems. Professor at ...
- **[Mix Irving](https://github.com/mixmix)**: Developer working on TinySSB, SecureScuttleButt and Ahau, and other decentralized technologies. Mix’s technical skills ensure that the tools we build are both robust and scalable for real-world use.
- **[Nico Pace](https://github.com/nicopace)**: Project leader and experimenter in decentralized technologies for firefighting and remote area communication. Nico’s fieldwork in Córdoba, Argentina, is crucial to tailoring these tools to the needs of firefighters.
- **[Luandro Viera](https://github.com/luandro/)**: Researcher and developer who has been experimenting with Meshtastic in the Amazon. His insights on real-world deployments are invaluable to our mission.
- **[Nanomonkey](https://github.com/nanomonkey)**: Contributor to SecureScuttleButt and TinySSB, focused on lightweight, offline-first solutions.

## Marketing

If you think this idea is worth spreading, we've developed a range of **marketing assets** that you can use to share about **WildfireSSB**'s mission to improve wildfire response in remote regions through open-source technology.

In this Google Drive you will find [our marketing assets](https://drive.google.com/drive/folders/1hC3ciOXWQaMKo56y4kgFO1V1ObuJ24Vg?usp=sharing) to download:

- Social media graphics (for Twitter, Instagram, and Facebook)
- Videos showcasing how the technology works
- Infographics explaining decentralized communication for firefighters

Feel free to share these materials and help us get more people involved in supporting this important cause!

## How You Can Contribute

We need your support to make this project a reality! Here's how you can get involved:

- **[Donate through Gitcoin](https://explorer.gitcoin.co/#/round/42161/608/115)**: Your contributions will directly support the development, testing, and deployment of these lifesaving tools. Plus, your donations will be matched by Gitcoin’s grant round, making every contribution even more impactful.
- **[Contribute to the code](https://github.com/ssbc/tinySSB)**: If you're a developer, join our community and help us build robust, open-source tools for wildfire response.
- **Spread the word**: Share our project on social media, tell your friends, or write a blog post. Every bit of awareness helps.
- **Design and community engagement**: Help us create educational resources, training materials, or work on UI/UX design to make the system easy to use.

Together, we can make a real difference in the fight against wildfires, protecting both people and the environment.

---

Join us in building a resilient future for wildfire response! #gg22 #wildfire #tech #oss #p2p #ATAK
