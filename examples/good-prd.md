# Reporting Dashboard

## Overview

The Reporting Dashboard enables business users to create, save, and share operational reports.

## Requirements

1. Users shall create reports using predefined templates.

2. Users shall export reports in CSV format.

3. Users shall share reports with users belonging to the same business unit.

4. Dashboard pages shall load within 3 seconds for datasets containing up to 100,000 records.

5. Authentication shall be provided through the corporate SSO platform.

## Acceptance Criteria

### Report Creation

- User can create a report using a template.
- Report is saved successfully.
- User receives confirmation message.

### Export

- User can export report to CSV.
- Export completes within 30 seconds.

### Performance

- Dashboard loads within 3 seconds for supported dataset sizes.
