# Inconsistent Styles with Tailwind's @apply and Dynamic Classes

This repository demonstrates a bug where Tailwind CSS's `@apply` directive doesn't correctly update styles when the class containing `@apply` is dynamically added or removed using JavaScript. This leads to inconsistent styling on the page.

## Problem

When you use `@apply` to include styles from another class and then add or remove that containing class dynamically (e.g., through JavaScript), Tailwind's build-time processing might not reflect the change appropriately. The styles may fail to update, persist even after the class is removed, or be absent when the class is added.

## Solution

Instead of relying on `@apply` for dynamic class manipulation, use utility classes directly or consider employing a runtime styling solution, such as directly manipulating the `style` attribute or using a JavaScript-based styling library. This offers more control over the styling process.