# Module Study Notes: Pre Security

## Section: Computer Fundamentals

## 1. Inside a Computer System
- *CPU (Central Processing Unit):* The "brain" of the computer that executes instructions, performs calculations, and manages data flow.
- *RAM (Random Access Memory):* Fast, volatile short-term memory used to hold temporary data for active processes. Cleared when powered off.
- *Storage (HDD / SSD):* Non-volatile long-term storage for files and the OS. SSDs use flash memory (faster); HDDs use magnetic platters.
- *Motherboard:* Main circuit board connecting CPU, memory, storage, and peripherals using bus systems.
- *Power Supply Unit (PSU):* Converts high-voltage AC electricity from the wall outlet into low-voltage DC power for internal parts.
- *Expansion Cards & Peripherals:* Hardware added via PCIe slots (e.g., GPU, NIC) or external ports (keyboard, mouse, monitor).

## 2. Computer Types
- *Supercomputers:* High-performance computing systems designed for complex mathematical simulations, weather forecasting, and scientific research.
- *Mainframes:* Enterprise-grade computers optimized for high-volume bulk data processing, transaction handling, and maximum uptime.
- *Desktops & Laptops:* Personal computers designed for individual end-user daily computing and productivity tasks.
- *Mobile & Wearables:* Low-power portable devices (smartphones, tablets, smartwatches) running optimized mobile operating systems.
- *Embedded Systems:* Special-purpose single-function computers embedded into non-computer devices (e.g., IoT chips inside coffee machines, cars, routers).

## Section Code Examples

```python
# 1. System Info Simulation (RAM vs Storage)
system_specs = {
    "CPU": "8-Core Processor",
    "RAM_GB": 16,        # Volatile Short-Term
    "Storage_GB": 512,   # Non-Volatile Long-Term
    "Is_SSD": True
}

print("System Hardware Summary:")
for component, detail in system_specs.items():
    print(f"- {component}: {detail}")
# Output:
# System Hardware Summary:
# - CPU: 8-Core Processor
# - RAM_GB: 16
# - Storage_GB: 512
# - Is_SSD: True

# 2. Categorizing Computer Types by Role
devices = {
    "Smartphone": "Mobile Device",
    "Smart Thermostat": "Embedded System",
    "Banking Core Server": "Mainframe",
    "Weather Simulator": "Supercomputer"
}

for device, category in devices.items():
    print(f"{device} -> {category}")
# Output:
# Smartphone -> Mobile Device
# Smart Thermostat -> Embedded System
# Banking Core Server -> Mainframe
# Weather Simulator -> Supercomputer
