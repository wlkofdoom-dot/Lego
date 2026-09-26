# Lego: Modular Docker Homelab Setup

This repository contains my personal, evolving Docker configuration stack. My goal with this project is to perfect a modular, friction-free deployment that I can stand up on any host system at a moment's notice.

I am sharing my setup and progress publicly so others can draw inspiration, adapt individual stacks, or replicate the environment.

---

## 🛠️ How to Use This Setup

If you want to deploy or test this configuration, **you must execute the steps in numerical order from `0` to `10`**. Each file builds on the storage structures, network interfaces, and container dependencies created in the preceding steps.

1. **Prerequisites & Scripts:** Run the system initialization and SMB mount scripts first to establish host paths and credentials.
2. **Network Creation:** Initialize the core MacVLAN networks (`macvlan-net-a` and `macvlan-net-b`) before spinning up any compose stacks.
3. **Container Stacks:** Bring up the stacks sequentially as numbered (Management, Filtering, Media, Downloaders, Utilities).

---

## 🔒 Security & Sanitization Note

To safely publish this project publicly, **all network names, static IP addresses, subnets, and sensitive credentials have been scrubbed and sanitized using AI**. 

Before deploying this on your own machine:
* Update the MacVLAN subnet and gateway configurations in Step 1 to match your physical network adapter and IP scheme.
* Provide your own SMB credentials in `/root/smbcred`.
* Adjust volume paths if your host storage mount points differ from the defaults.

---

## 📄 License & Usage

Feel free to fork, adapt, or copy any part of these stacks for your own homelab setup.
