# Silos

**Enterprise data silos cost money quietly.**

A container sits stuck at port for six days. Shipping ops knows it's 
stuck. Finance knows there's a penalty clause. Neither system talks 
to the other — so nobody knows it's already cost ₹84,000 until the 
invoice arrives.

CargoBridge is an MCP agent that closes that gap in real time.

## What it does

1. **Inspects** — autonomously detects delayed shipments in the logistics system
2. **Calculates** — reads raw contract clauses from the finance system, 
   interprets which one applies, computes the live penalty
3. **Acts** — dispatches backup transport instead of sending an alert

## Why an agent, not a script

Contract clauses are ambiguous: tiered rates, grace periods conditional 
on fault attribution, force majeure wording that may or may not apply. 
Deciding *which clause governs a given situation* is judgment, not lookup.

The `logistics` and `finance` modules share no imports, no types, and no 
data. The agent is the only thing bridging them — the silo is real, not 
simulated.

## Built with

- [NitroStack](https://nitrostack.ai) — TypeScript MCP framework
- Model Context Protocol
- React widgets for incident rendering

> Built for the NitroStack MCP Hackathon at SRMIST.
