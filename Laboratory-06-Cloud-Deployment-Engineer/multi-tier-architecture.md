# Multi-Tier Architecture

## What Is a Two-Tier Architecture?

A two-tier architecture splits an application into two separate layers, each with its own responsibility. The first tier handles everything the user interacts with and the application logic, while the second tier is dedicated to storing and managing data. The two tiers communicate over a network, which lets each one be built, deployed, and maintained independently.

## The Web/Application Tier

The web/application tier is the part of the system that users reach directly. Its role is to serve the user interface, handle incoming HTTP requests, run the application logic, and process what users submit (such as logging in or uploading a file). It does not store data permanently. Instead, it asks the database tier for the data it needs and returns the result to the user.

In this lab, the Nextcloud container is the web/application tier.

## The Database Tier

The database tier is responsible for storing persistent data, meaning information that must survive restarts and be available later. This includes user accounts, passwords (stored securely), file metadata, settings, and sharing permissions. It also handles queries from the application tier, enforces data integrity, and manages backups.

In this lab, the MariaDB container is the database tier.

## Why Separate Them?

Keeping the web server and the database in two separate containers is better than packing both into one because each can be scaled, updated, and restarted on its own without affecting the other. It also improves security, since the database can be kept off the public network and exposed only to the application tier. Finally, it makes troubleshooting easier and follows the container best practice of one service per container, so a failure in one component does not take down the whole system.
