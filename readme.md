Cyber Gauntlet CTF

Overview

Cyber Gauntlet CTF is a Capture The Flag (CTF) environment designed to provide users with an interactive cybersecurity challenge. The environment includes an attacker machine and a vulnerable victim machine, where players can conduct reconnaissance, exploit vulnerabilities, and retrieve hidden flags. A CTFd platform is used to manage scoring and flag submission.

This setup is built using Docker Compose, allowing for a portable and easily deployable CTF environment.

Current Setup

The initial setup consists of the following Dockerized components:

Kali Attacker Machine – A penetration testing workstation using the official Kali Linux Docker image.

Ubuntu Victim Machine – A basic Linux environment that will be configured with vulnerabilities in future versions.

CTFd Scoring Platform – A self-hosted instance of CTFd to manage challenge submissions and scoring.

All components run within a dedicated Docker network, ensuring seamless communication for the attack scenarios.

Task List

Create an Attacker Machine

Uses the kalilinux/kali-rolling Docker image.

Configured to allow interactive terminal access.

Create a Victim Machine

Currently uses an ubuntu:latest image.

Future iterations will include pre-configured vulnerabilities.

Deploy Capture The Flag Platform (CTFd)

Hosted via the ctfd/ctfd Docker image.

Accessible via http://localhost:8000 for flag submission.

Future Enhancements

Replace the base victim machine with a pre-configured vulnerable environment.

Introduce a Windows-based victim machine.

Add persistent storage for attack progress tracking.

Automate flag generation and placement within victim machines.

Getting Started

Prerequisites

Docker & Docker Compose installed.

Deployment

Run the following command to deploy the environment:

docker-compose up -d

Accessing the Components

Kali Attacker Machine:

docker exec -it kali_attacker /bin/bash

Ubuntu Victim Machine:

docker exec -it ubuntu_victim /bin/bash

CTFd (Scoring Platform):Open http://localhost:8000 in your browser.

