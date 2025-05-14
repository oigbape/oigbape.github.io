---
title: "zk-creds-demo"
order: 1
excerpt: "Demonstrated a flexible anonymous credential system using zkSNARKs (Groth16, Poseidon hash) and the zkcreds-rs library for privacy-preserving verification of attributes such as age on passport data."
collection: portfolio
#date: "2025-04-24"
tags: [Cybersecurity, Cryptography, zkSNARKs, Anonymous Credentials, Privacy, Rust, Zero-Knowledge Proofs, Identity Management] 
technologies: "zkSNARKs (Groth16), Rust (zkcreds-rs), Poseidon Hash, Merkle Trees, NFC (concept)"
#github_url: "[Link to your GitHub repo for zk-creds]"
# report_url: "[Link to PDF report if available]"
# image_path: "/images/portfolio/zk-creds-teaser.png" # Add a teaser image
---

## Objective
This project aimed to address the privacy challenges in traditional user authentication by implementing and evaluating an anonymous credential system based on core zk-creds principles. The specific use case was to enable a user to prove they are over 21 years old using the Date of Birth (DOB) from their passport (accessed conceptually via NFC) without revealing the actual DOB or other Personally Identifiable Information (PII).

## Role & Contributions
* Collaborated on researching foundational concepts of Anonymous Credentials (AC), the zk-creds system by Rosenberg et al. (2023), and enabling technologies like zkSNARKs (Groth16) and the Poseidon hash function.
* Contributed to the design of the system flow, including credential issuance using Merkle trees, presentation with zero-knowledge proofs, and verification against a defined predicate (age > 21).
* Worked with the `zkcreds-rs` Rust library to implement the core cryptographic operations for the age verification demo.
* Involved in setting up the demonstration scenario, which conceptually utilized passport data (read via NFC) as the source of attributes for credential issuance and blinding.
* Analyzed and documented the privacy guarantees of the system, particularly anonymity and unlinkability, as well as aspects of auditability provided by the zk-creds model.
* Co-authored the final project report detailing the problem context, related concepts, implementation, demo setup, and conclusions.

## Technologies & Concepts Applied
* **Cryptography:** Zero-Knowledge Succinct Non-interactive Arguments of Knowledge (zkSNARKs - Groth16 scheme), Poseidon Hash Function, Merkle Trees, Blind Groth16 proofs.
* **Programming Language:** Rust (via the `zkcreds-rs` library).
* **System Design:** Anonymous Credential lifecycle (Issuance, Presentation, Verification).
* **Identity Concepts:** Privacy-Preserving Authentication, Personally Identifiable Information (PII) protection, attribute-based credentials.
* **Data Source Concept:** Passport data via Near Field Communication (NFC).

## Key Outcomes & Learnings
* Successfully demonstrated a functional anonymous credential system for age verification, showcasing the practical application of zk-creds.
* Gained hands-on experience with the `zkcreds-rs` library and the practical implementation aspects of zkSNARK-based systems.
* Developed a deep understanding of how Merkle trees and zero-knowledge proofs can ensure credential validity and user anonymity simultaneously.
* The project highlighted the potential of advanced cryptographic techniques to enhance user privacy in digital interactions, moving beyond traditional identification methods.

## Artifacts
* **Project Repository:**  
* **Project Report:**  
