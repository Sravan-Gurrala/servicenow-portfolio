# Project 4: IT Asset Request Portal & Data Management

## Overview
Self-service portal assets, bulk data import pipelines, and executive reporting.

## What Was Built
- **Record Producer:** `Report Asset Issue` mapping end-user inputs directly to the `Incident` target table.
- **Order Guide:** `New Hire IT Hardware Package` bundling hardware requests into one checkout.
- **Data Import Pipeline:** Uploaded CSV file to staging table (`u_sample_users_import`), mapped fields via Transform Map, and set `Coalesce` on `Email` to update existing users without creating duplicates (verified 1 Insert, 1 Update).
- **Reports & Dashboards:** Built Pie, Single Score, and Bar charts, publishing them on a unified `IT Operations & HR Dashboard`.

## Structure
- `/screenshots/`: Screenshots of Record Producer, Order Guide, Transform Map with Coalesce, Import results, and Dashboard.
