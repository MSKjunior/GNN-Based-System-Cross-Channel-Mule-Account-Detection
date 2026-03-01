# GNN-Based-System-Cross-Channel-Mule-Account-Detection
A Graph Neural Network (GNN) based system for detecting mule accounts across multiple financial channels. Mule accounts are intermediary bank accounts used by criminals to launder money or facilitate fraud. This system leverages the power of graph-based deep learning to identify suspicious account patterns across different transaction channels.
# 🔎 Cross-Channel "Mule Account" Detection Graph 

> *GNN-powered real-time transaction monitoring* that fuses App, Web, ATM &
> UPI log streams into a unified Entity Graph to detect and block money-mule
> rings before funds leave the network.

---

## 📋 Problem Statement

Money mules operate across channels to hide their tracks — receiving money via
a *Mobile App, moving it to a **Linked Wallet*, and **withdrawing cash at
an ATM** within minutes. Traditional siloed fraud rules miss these
high-velocity, cross-channel patterns.

## 🎯 Solution Architecture
┌─────────────┐ ┌─────────────┐ ┌─────────────┐ ┌─────────────┐
│ App Logs │ │ Web Logs │ │ ATM Logs │ │ UPI Logs │
└──────┬───── ┘ └──────┬──────┘ └──────┬──────┘ └──────┬──────┘
│ │ │ │
└────────────────┴──… 
# 🔎 Cross-Channel "Mule Account" Detection Graph

> *GNN-powered real-time transaction monitoring* that fuses App, Web, ATM &
> UPI log streams into a unified Entity Graph to detect and block money-mule
> rings before funds leave the network.

---

## 📋 Problem Statement

Money mules operate across channels to hide their tracks — receiving money via
a *Mobile App, moving it to a **Linked Wallet*, and **withdrawing cash at
an ATM** within minutes. Traditional siloed fraud rules miss these
high-velocity, cross-channel patterns.

## 🎯 Solution Architecture
┌─────────────┐ ┌─────────────┐ ┌─────────────┐ ┌─────────────┐
│ App Logs │ │ Web Logs │ │ ATM Logs │ │ UPI Logs │
└──────┬───── ┘ └──────┬──────┘ └──────┬──────┘ └──────┬──────┘
│ │ │ │
└────────────────┴────────────────┴────────────────┘
│
┌───────────▼───────────┐
│ Kafka Ingestion │
│ (Unified Schema) │
└───────────┬───────────┘
│
┌───────────▼───────────┐
│ Entity Graph │
│ (Neo4j + NetworkX) │
└───────────┬───────────┘
│
┌───────────▼───────────┐
│ GNN Model Engine │
│ (PyTorch Geometric) │
│ • Relationship │
│ Scoring │
│ • Velocity Detection│
│ • Mule Cluster ID │
└───────────┬───────────┘
│
┌───────────────┼───────────────┐
│ │ │
┌────────▼──────┐ ┌─────▼──────┐ ┌──────▼───────┐
│ FastAPI │ │ Alert │ │ Regulator │
│ Real-time API │ │ Engine │ │ Reports │
└────────┬──────┘ └────────────┘ └──────────────┘
│
┌────────▼──────┐
│ Next.js │
│ Dashboard │
└───────────────┘
