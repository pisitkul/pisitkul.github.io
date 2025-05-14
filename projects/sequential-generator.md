---
layout: project
type: project
image: img/seq-square.png
title: "Sequential Generator"
date: 2025
published: true
labels:
  - Node.js
  - TypeScript
  - npm
  - Open Source
  - dayJs
summary: "A Node.js module for generating unique, date-prefixed sequential codes with timezone support"
---

# Sequential Generator

<div style="text-align: center;">
  <img src="../img/seq-generator-header.png" alt="Sequential Generator Banner">
</div>

## 🛠 What is Sequential Generator? (EN)

In small applications, we often need a way to generate document IDs like invoices (`INV`) or order numbers with a clear date and sequence. **Sequential Generator** is designed to:

- **Generate unique codes** by incrementing from the previous one
- **Provide ordered codes** per day
- **Include date information**
- **Support TimeZones** such as `Asia/Bangkok`, `UTC` (powered by [`day.js`](https://day.js.org/))

## How to Use 

[sequential-generator](https://www.npmjs.com/package/sequential-generator) is an open-source Node.js module that generates customizable document codes with date prefixes.

ตัวอย่าง:  
```plaintext
SEX2505140001 → Generated on May 14, 2025 with prefix "SEX" and sequence "0001"
```

## 🔑 Features 
- ✔  Format – Define {prefix}{date}{sequence}
- 🌍 TimeZone Support – e.g., Asia/Bangkok, America/New_York
- 📅 Flexible Date Format – e.g., YYMMDD, YYYYMM
- 🔢 Custom Sequence Length – e.g., 0001 for 4 digits
- 🛠  Validation – Check and extract date from code
- ⏭ Auto Increment – Generate the next code in sequence

``` js
import SequentialGenerator  from 'sequential-generator';

// Create a generator with prefix, timezone, default date format and sequence length
const generator = new SequentialGenerator('SEX', 'Asia/Bangkok');

// Generate a new code
const newCode = generator.generate();
console.log(newCode);  // Example output: SEX2305110001

// Validate a code
const isValid = generator.validate('SEX2305110001');
console.log(isValid);  // true or false

// Increment an existing code
const incrementedCode = generator.increment('SEX2305110001');
console.log(incrementedCode);  // Example output: SEX2305110002

```

### Max Limit

```js
const maxCode = 'SEX2305119999';  // Maximum for 4-digit sequence
try {
  console.log(generator.increment(maxCode));
} catch (error) {
  console.error(error.message);  // Output: "Maximum number reached. Cannot increment."
}
```


