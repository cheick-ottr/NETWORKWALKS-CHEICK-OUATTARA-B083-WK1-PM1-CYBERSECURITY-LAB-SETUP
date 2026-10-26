# NETWORKWALKS-CHEICK-OUATTARA-B083-WK1-PM1-CYBERSECURITY-LAB-SETUP

# 🔒 Cybersecurity Lab Environment Setup

Building an isolated virtual lab for penetration testing and ethical hacking practice

## 🛠️ Project Overview
This project focuses on setting up a virtual cybersecurity and penetration-testing laboratory using **Oracle VirtualBox** and **Kali Linux**. The purpose of the lab is to create a controlled environment where cybersecurity tools, network scanning, reconnaissance, vulnerability assessment, and other security-testing activities can be performed safely and repeatedly.

## 📋 Lab Specifications & Configuration Details
* **Base Virtualization:** Oracle VirtualBox v7.2.22
* **Attacking Machine:** Kali Linux v2026.3 .
* **Network Type:** NATNetwork (`10.0.0.0/24`).
* **Kali Linux IP Address:** `10.0.0.2/24` (Static IP).
* **Gateway & DNS:** Gateway `10.0.0.1`, DNS `8.8.8.8`.
* **Convenience Features:** Shared Clipboard & Drag'n'Drop enabled (Bidirectional), Shared Folders (`/downloads`) configured.

## 📸 Lab Implementation & Screenshots

### 1. Configuration du Réseau NATNetwork (`10.0.0.0/24`)
<img width="960" height="1080" alt="Reseau NATNetword" src="https://github.com/user-attachments/assets/e7ecf02a-4c13-45bf-aa4e-fed1706b215c" />

### 2. Paramètres Réseau de la Machine Kali Linux
<img width="960" height="1080" alt="setting kali" src="https://github.com/user-attachments/assets/ddfff1cc-6119-4bed-ab1d-93a6b953ed08" />

### 3. Test de Connectivité et Résolution (Ping Réussi)
<img width="1282" height="907" alt="pingg" src="https://github.com/user-attachments/assets/c77fd5d7-b3a5-4dda-af63-9e90e812ebed" />

## 🔍 Troubleshooting (Résolution du problème réseau)
Pour résoudre le problème courant de connectivité Internet (*Network is unreachable*) sur les versions récentes de Kali Linux et VirtualBox v7, la commande suivante a été appliquée avec succès :
```
sudo nmcli connection modify "Wired connection 1" ipv4.dad-timeout 0
sudo nmcli connection down "Wired connection 1"
sudo nmcli connection up "Wired connection 1"
