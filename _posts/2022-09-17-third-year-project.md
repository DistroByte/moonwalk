---
layout: post
author: James Hackett & Alexandru Dorofte
---

# Third Year Project Blog

We're writing this to help future people with their Third Year Project and also to keep track of what we're doing so we can look back on it and reflect.

## Securing a Supervisor and Project

##### James Hackett

Myself and Alex had decided we wanted to be project partners in June at the end of second year, and we sent a message to Steve Blott not long after that. We had both come up with ideas we wanted to pursue and we both though they could do well. We decided to let Blott decide what he wanted to pick as "his project". He ended up latching onto my idea; home automation based bluetooth triangulation.

We spent the summer working out kinks in the idea, and we had a rough idea of what we wanted to do to describe to Blott in out in person meeting. Blott had told us we were super early and to come and talk to him right at the start of Semester 1, so we did that.

The first Tuesday of Semester 1, myself and Alex showed up to Blott's office and discussed our idea. He was very on board with the idea, but suggested some changes to make it more third-year-project-like. He suggested that our demo should consist of us walking around the lab and turning lights on and off as we walk. This would involve interfacing with the lights at a hardware level (using zigbee) and also working with the code to figure out where the tracked device actually is, with information taken from some Raspberry Pi Pico W boards usuing some form of radio or wireless.

Our demo would be both flashy and easy to cover parts that didn't work.

## Testing Pico W Boards

##### Alexandru Dorofte

Right after our meeting with Blott our Supervisor, we bought a couple of Pico W boards and began testing them. The reason we chose these boards is because they are in stock and very cheap to acquire, unlike other hardware.

We found so many different versatile uses for these boards. One interesting use was turning them into a Human Interface Devices (HID). This allowed us to use the boards as a keyboard or mouse input. Giving us the ability running scripts to play pranks on our peers' laptops.

However, when trying to access the boards' bluetooth capabilities we ran into some problems.

We noticed very quickly that there were some limitations with the boards. At the time of testing the boards were running on a version that did not feature bluetooth support, only wifi. This did not matter as we found out that even if we were able to access the bluetooth capabilities, the range was very limited and accuracy was not suitable for our project, wifi included.

We had to find a different way to achieve our goal of having an accurate reading. So we had to look for other hardware that would be able to do the job.

## UWB CHIPS

##### James Hackett

This was the first hurdle of our project, we had hoped to use the Pico W boards to do what we wanted, but we were wrong. We had to find a new way to achieve accurate location data. 

This is where I found out about UWB chips. UWB is a radio technology that uses very short pulses of radio waves to transmit data. This allows for very accurate location tracking, and it's also very power efficient.
The hardware was a bit more expensive than the Pico W boards, and quite new to the market, but it was the only way to get the accuracy we needed.

We found out about Decawave, a company based in Ireland that makes UWB chips. However they were acquired by another company, called Qorvo. Most of the documentation and information was difficult to find. After a lot of searching we found out that we could buy development kits from a third party vendor based in Ireland.

## Project Proposal

##### Alexandru Dorofte

After we had decided on the hardware we wanted to use, we had to write a project proposal. This was a document that we had to submit and present to an approval board. The proposal outlined the plan for the project and the goals we wanted to achieve. It also included a timeline of the project.

After meeting with thr board, our project was approved and we were given the go-ahead to start working on the project. They were quite interested in our idea and were very supportive of our project.

Overall we felt very confident about our project and we were very excited to get started.

## Buying Hardware (PROBLEM)

##### Alexandru Dorofte

Like all things in Life, nothing is as easy as it seems. We bought a UWB transceiver, the DWM3001CDK development kit, from a third party vendor in Ireland. We were ready to begin the project, but we were in for a nasty surprise.

There was no support for Android or easy access to the hardware. The development kits after much digging were only supported by Apple and their Apple U1 chip. This was a huge problem as we had no way of accessing the hardware. It seemed that Qorvo, also a supplier for Apple, had locked support. After much digging and deliberation, we decided that the DWM3001CDK was not going to be suitable for our project.

This was a problem and so we had to scrap this hardware and had to look for other ways to obtain UWB hardware. This was a huge blow to our motivation and so the hunt for other hardware began.

## Zigbee (Conbee)

##### James Hackett

We put aside for the time being UWB chips and decided to look into the Zigbee protocol. Which would allow us to control smart home devices that operate on this protocol. As such we bought a Conbee II stick, which is a USB dongle that allows you to connect Zigbee devices to your computer.

Zigbee is a home automation protocol that allows you to control devices such as lights, sensors, and switches. It's a very popular protocol and is used in many smart home devices. It's also very easy to use and there are many libraries available for it.

The Conbee II stick allows for easy communication with these devices, acting as a hub for them to connect to. Because of its open source nature, it would be easy to integrate into our project.

## Buying new UWB sensors (Problem Solved)

##### Alexandru Dorofte

After a lot of searching, we had 2 options for UWB hardware. First was an expensive development kit that would take a fair amount of time on delivery. The second option buying from the same vendor. It would be an older version of the hardware we had before which was made before Qorvo acquired the original manufacturer.

We decided to go with the second option as it was cheaper and we could get it delivered faster. We bought the DWM1001-DEV development kit, which was the older version of the DWM3001CDK. When the hardware came I tested and got the devices to work with each other. This was a huge relief as we could finally get started on the project.

## Anchor Python

##### James Hackett


## API and Localization

##### James Hackett

## Final Blog Post

##### Alexandru Dorofte & James Hackett

