---
sidebar_position: 1
---

# Basic Tailscale Setup

These instructions will help you create a Tailnet and connect an Unraid server. Once finished, you should be able to
connect to the following services via the Tailscale IP / MagicDNS name of the Unraid server:

- WebGUI
- File shares (SMB/NFS)
- SSH
- Bridge mode Docker containers (default or custom bridge networks)

!!! note
    Docker containers running on ipvlan/macvlan networks (e.g., br0) cannot be accessed via the Tailscale IP for the
    Unraid server. To connect to these containers, you should either [configure a subnet router](advanced-tailscale-settings.md) or 
    [add Tailscale to the container](connecting-docker-containers.md).

## Create a Tailnet

1.  Go to [Tailscale](https://www.tailscale.com) and click the **Get Started** button.

    ![](../../assets/tailscale/get-started.png)

2.  Select an identity provider and log in.
   
    ![](../../assets/tailscale/identity-provider.png)

3.  Select either **Business use** or **Personal use**.

    ![](../../assets/tailscale/personal-use.png)

4.  Follow the provided instructions to install Tailscale on a client device (phone/laptop/etc.).

    ![](../../assets/tailscale/first-device.png)

5.  Once you have installed Tailscale on the device, it will appear on the screen.

    ![](../../assets/tailscale/second-device.png)

## Install the Unraid Tailscale Plugin

1.  Log in to the Unraid server and switch to the **Apps** tab.
2.  Search for **Tailscale**.
3.  Install **Tailscale (Plugin)**.

    ![](../../assets/tailscale/install-plugin.png)

4.  Click **Done** once the window shows that Tailscale has been installed.

    ![](../../assets/tailscale/install-complete.png)

5.  Switch to the **Settings** tab, then click on **Tailscale**.

    ![](../../assets/tailscale/settings-menu.png)

6.  Click **Reauthenticate**.

    ![](../../assets/tailscale/reauthenticate.png)

7.  Click **Connect**.

    ![](../../assets/tailscale/connect-device.png)

8.  After the connection is complete, the browser will redirect to the Tailscale admin console, which should show both
    devices are connected.

    ![](../../assets/tailscale/tailscale-console.png)
