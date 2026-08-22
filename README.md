# Textile R&D Calculations

A lightweight browser-based **Textile R&D Calculation Tool** designed to simplify common textile yarn, fabric, costing, and count-related calculations.

The application is built as a standalone HTML file using **HTML, CSS, and JavaScript**, with client-side PDF generation through **jsPDF** and **jsPDF-AutoTable**.

## Overview

Textile R&D Calculations provides a single dashboard for performing commonly used calculations during textile product development, yarn analysis, fabric development, costing, and technical evaluation.

The application works directly in the browser and does not require a backend server or database.

### Main Modules

1. **Yarn Consumption Calculation & Composition**
2. **Price Idea Sheet**
3. **Price Conversions**
4. **Count Calculation**
5. **Yarn Count Conversion**

The application also supports dynamic rows and PDF report generation.

---

## Features

### 1. Yarn Consumption Calculation & Composition

The Yarn Consumption module allows users to enter multiple yarn components and calculate their relative consumption.

Each yarn entry can include:

- Yarn number
- Yarn count (Ne)
- Stitch/SL value
- Feed ratio
- Up to 5 material components
- Material percentage for each component
- Calculated yarn consumption percentage

The system also generates an overall **Fabric Composition** based on the yarn consumption and material percentages.

Users can:

- Add additional yarn rows
- Remove yarn rows
- Enter different material combinations
- View calculated consumption percentages instantly
- Generate a PDF report

The initial interface contains three yarn rows, with the ability to dynamically add more. :contentReference[oaicite:1]{index=1}

---

## 2. Price Idea Sheet

The Price Idea Sheet is designed for preliminary fabric costing.

It includes:

### Yarn Details

- Yarn count / description
- Consumption percentage
- Yarn unit price ($/Kg)
- Calculated yarn price ($/Kg)
- Combined yarn price

Additional yarn rows can be added or removed dynamically.

### Knitting Details

Users can enter:

- Knitting structure
- Knitting charge ($/Kg)

Multiple knitting rows are supported.

### Preprocess / Dyeing / Finishing

The module supports:

- Process name
- Process type
- Process charge ($/Kg)

Additional process rows can be added dynamically.

### Final Costing

The application calculates:

- Total fabric price
- Process loss
- Price after process loss
- Profit
- Finished fabric price

The current implementation calculates yarn, knitting, and process costs before applying process loss and profit. :contentReference[oaicite:2]{index=2}

---

## 3. Price Conversions

The Price Conversion module converts fabric prices between:

- **$/Kg**
- **$/Yd**

The calculation uses:

- Fabric price
- Fabric width in inches
- Fabric GSM

The interface supports two conversion directions:

```text
$/Kg → $/Yd
$/Yd → $/Kg
