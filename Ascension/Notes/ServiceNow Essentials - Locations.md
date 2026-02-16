09-24-2025 22:47

Tags: [[ServiceNow]] [[GRC]]

## Locations

These are the physical sites of Ascension

### Location Data Sources

SNow pulls location info from 3 sources:

- **Medexcel** - floor and room data
- **Legacy SNow platform** - Contains existing location list
- **PeopleSoft** - Supplies some location details

Users are assigned a location identifier (ERP ID) by SailPoint. The ERP IDs correspond to facilities. 

### Location Hierarchy

Location hierarchy is arranged as follows: 

- Region, City, Campus, Building, Floor, Room

This hierarchy is used to assign associate locations in Snow for:

- Incidents
- Problems
- Change Requests
- Demands
- Ideas
- Project and Project Tasks

### Location Lifecycle Stages and Statuses

#### Ideation

- Lifecycle Stages Statuses - Chartered, Build
- Locations that are planned but not yet built or operational. 

#### Operational

- Lifecycle Stage Statuses - Available, In Use, Pending Retirement
- Locations actively in use or available.

#### End of Life

- Lifecycle Stage Statuses - Sold, Lease Return, Obsolete
- Location is no longer in use and has been disposed of, closed. 

## References

[[ServiceNow Essentials]]
