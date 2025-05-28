# Lab: TCP 3-Way Handshake

**Date:** 2025-05-28
**Tool:** Wireshark  
**Topic:** TCP Session Initiation

## 🧠 Goal

Visually identify the SYN → SYN-ACK → ACK sequence in Wireshark.

## 🔍 What I Did

- Visited `http://neverssl.com`
- Filtered with `tcp.flags.syn == 1`
- Followed the TCP stream between my IP and server IP

## 📦 Packet Findings

- Packet 12: SYN from 192.168.1.5 to 34.117.59.81 (port 80)
- Packet 13: SYN-ACK from 34.117.59.81 to 192.168.1.5
- Packet 14: ACK from 192.168.1.5 — handshake complete

## ⚠️ Surprises

- Saw multiple ACK packets being sent after the handshake
- Connection finalised with [FIN, ACK] packet
