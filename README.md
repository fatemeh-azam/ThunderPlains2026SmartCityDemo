# When Every Device Speaks a Different Language

**Building Resilient Event-Driven Systems** · ThunderPlains 2026, Oklahoma City · Fatemeh Azam

▶ **[Watch the demo in your browser](https://fatemeh-azam.github.io/thunderplains-2026-demo/)**

This repository accompanies my ThunderPlains 2026 talk. It contains the slides and a static, browser-only walkthrough of the four live demos. Everything in the demo is scripted with synthetic data.

> **No production code here.** The talk was based on a research testbed at the Oklahoma Cyber Innovation Institute (OCII), The University of Tulsa. That system and its data are not part of this repository. The demo page is a standalone illustration written for this repo: one HTML file, no backend, no dependencies.

## What's in this repository

| | |
|---|---|
| [`index.html`](index.html) | The demo: a scripted, self-contained page that plays the four demo scenarios with synthetic data |
| [`slides/`](slides/) | The talk slides (PDF) |

## The talk

Drones, sensors, GPS receivers and browsers all speak different languages: different radios, formats, clocks and failure modes. The talk walks through a smart city testbed where all of them share one event bus, and the five patterns that kept it calm.

1. **Publish, don't call.** Every device publishes to one bus. Nothing talks to anything else directly, so a new device needs no new code.
2. **Translate once, at the door.** Every reading is checked and reshaped into one message shape as it arrives, never again downstream.
3. **The timestamp is sacred.** Stamp each reading where it was measured. Arrival time lies when messages are retried or batched.
4. **One cause, one alert.** Wait until a problem has lasted, group symptoms by their root cause, and clear only past a margin. Alert fatigue is a design bug.
5. **Silence is data.** A device that stops talking is telling you something. Judge that silence against what it should be doing.

The same patterns apply well beyond drones: microservices on queues, webhooks from many vendors, CI pipelines, and apps that mix REST, WebSockets and webhooks.

## The demo

Open the [live demo](https://fatemeh-azam.github.io/thunderplains-2026-demo/), or download `index.html` and open it in any modern browser. It plays four chapters (about two minutes in all), with play, pause, speed and chapter controls:

1. **A calm city.** Six different devices publish to one bus, in one message shape.
2. **Radio interference.** Four Wi-Fi devices degrade one after another; the operator sees one grouped incident, not a flood of alerts. GPS and the 433 MHz alarm stay healthy.
3. **A sensor goes quiet.** Five seconds without data is an event: the card greys out and shows when the sensor was last heard from.
4. **A hijacked delivery.** Two drones fly delivery missions registered before takeoff. One is pulled off its route; because the system knows each mission, it raises one clear alert and tracks the drone back.

Watch the two counters: hundreds of readings arrive, and only a handful of events reach a person.

## Related research

- *Authority Contention in Micro-UAV Command Stacks*, Fatemeh Azam and Cameron Alred, IEEE Cyber Awareness and Research Symposium (CARS) 2026. Publication link coming soon.

## About

Fatemeh Azam, Senior Software Engineer and Researcher, Oklahoma Cyber Innovation Institute (OCII), The University of Tulsa.
More about my projects: [your website](https://example.com)

© 2026 Fatemeh Azam. Shared for viewing and learning; please ask before reusing the slides or the demo.
