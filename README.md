# 🚀 Laravel 12 REST API - Product Management

A clean and scalable **RESTful API** built with **Laravel 12**, MySQL, and Eloquent ORM.

This project demonstrates a complete CRUD implementation with **One-to-Many database relationships**, request validation, eager loading, RESTful API routing, and structured JSON responses.

> 🎯 Built as a portfolio project to demonstrate Laravel Backend Development skills.

---

## 📌 Project Overview

This API provides a simple Product Management system where:

- A **Category** can have many Products.
- A **Product** belongs to one Category.
- Users can create, read, update, and delete Categories.
- Users can create, read, update, and delete Products.
- Product data can be retrieved together with its Category.
- Category data can be retrieved together with its Products.

### Database Relationship

```text
┌─────────────────┐
│   Categories    │
├─────────────────┤
│ id              │
│ name            │
│ description     │
└────────┬────────┘
         │
         │ 1
         │
         │ hasMany
         │
         │ N
┌────────▼────────┐
│    Products     │
├─────────────────┤
│ id              │
│ category_id     │ ◄── Foreign Key
│ name            │
│ description     │
│ price           │
│ stock           │
└─────────────────┘