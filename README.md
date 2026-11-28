### Ravindra JOB — Systems, Cloud & Self-Hosted Infrastructure

Cloud & SRE engineer building lightweight, fail-closed open-source tools for Linux, Matter/Thread, Home Assistant, self-hosted AI, and 3D-printed homelab hardware.

[Blog & Benchmarks (FR)](https://blog.ravindra-job.fr) · [LinkedIn](https://www.linkedin.com/in/ravindrajob) · [Ko-fi](https://ko-fi.com/ravindrajob)

<table>
  <tr>
    <td align="center" width="50%">
      <a href="https://github.com/ravindrajob/thread2mqtt">
        <img src="https://raw.githubusercontent.com/ravindrajob/thread2mqtt/main/assets/demo_mesh_anim.gif" alt="Thread2MQTT Animated Thread Mesh Topology" width="100%" />
      </a>
      <br/><sub><b>thread2mqtt</b> — Rust <code>std</code> Thread/Matter debugger &amp; HA MQTT bridge</sub>
    </td>
    <td align="center" width="50%">
      <a href="https://github.com/ravindrajob/matter-echo-delta-exporter">
        <img src="https://raw.githubusercontent.com/ravindrajob/matter-echo-delta-exporter/main/assets/demo_dashboard.webp" alt="matter-echo-delta-exporter Passive Kernel BPF UI" width="100%" />
      </a>
      <br/><sub><b>matter-echo-delta-exporter</b> — Passive Linux BPF probe for Matter UDP/5540</sub>
    </td>
  </tr>
</table>

#### Flagship Open-Source Projects

| Repository | Stack | Footprint / Guardrails | Scope |
| :--- | :--- | :--- | :--- |
| [**thread2mqtt**](https://github.com/ravindrajob/thread2mqtt) | Rust `std` (0 crates) | `1.2 MB` bin · `~1.8 MB` RSS · RO default | Thread (OTBR) & Matter-over-Thread topology debugger, 2.4 GHz RF scan & HA MQTT bridge |
| [**matter-echo-delta-exporter**](https://github.com/ravindrajob/matter-echo-delta-exporter) | Rust `std` · Linux BPF | `574 KB` bin · `CapEff=0` post-BPF | Passive `UDP/5540` & `UDP/5353` kernel BPF exporter for encrypted Matter (`TX - RX` delta) |
| [**ephemeral-ssh-bastion**](https://github.com/ravindrajob/ephemeral-ssh-bastion) | Python · Docker · TOTP | `0 MB` RAM idle · 3-strike killswitch | Break-Glass ephemeral Web SSH (`Telegram` RBAC, 192-bit URL, `docker-socket-proxy`) |
| [**tg-llm-router**](https://github.com/ravindrajob/tg-llm-router) | Rust `std` (0 crates) | `814 KiB` bin · `< 1 MB` RSS · hot-reload | Telegram Multi-LLM (OpenAI/Claude/Gemini/Grok/Ollama) & local Markdown RAG router |
| [**ha-drift-sentinel**](https://github.com/ravindrajob/ha-drift-sentinel) | Python 3.12 · YAML | `< 25 MB` RAM · RO default | Golden State anti-drift sentinel for Home Assistant, Zigbee2MQTT & Matter bridges |
| [**dreameA2**](https://github.com/ravindrajob/dreameA2) | Three.js · FastAPI | Offline r160 · fail-closed `503` | Local 3D LiDAR (`.pcd`) WebGL cockpit & Home Assistant bridge (15k-pt synthetic demo) |
| [**impression_3d**](https://github.com/ravindrajob/impression_3d) | OpenSCAD · STL | Parametric · 0% support | Open-source 3D models: 19" homelab rack, smart home, EDC cards, radio/SDR & pottery |
| [**InfraAtHome**](https://github.com/ravindrajob/InfraAtHome) | Docker Compose | Hardened self-hosted examples | Home-Lab infrastructure stacks (Pi-hole, CrowdSec, Vaultwarden, NUT) |
| [**Observability-Monitoring**](https://github.com/ravindrajob/Observability-Monitoring) | Prometheus · Thanos · Grafana | Long-term metrics & alerting | Self-hosted observability, dashboards & alert rules |

#### Engineering Principles
- **Zero-crate Rust (`std`-only)** where it counts: static musl binaries, low RSS, minimal supply-chain surface.
- **Fail-closed & Zero-Trust by default:** `read_only_mode: true`, loopback binding (`127.0.0.1`), non-root read-only containers (`cap_drop: [ALL]`), zero direct `docker.sock`.
- **Offline-first & reproducible:** `0` external CDNs, 10-second `--demo` sandboxes, native Prometheus `/metrics` & Grafana dashboards.
