2024-10-02 19:41

Tags: [[Security]] [[CompTIA]] [[Fundamentals]] [[Security Attacks]] 
# Security+ Chapter 9 Implementing  Controls to Protect Assets

## Comparing Physical Security Controls

### Access Badges

Proximity cards are typically credit card-sized access cards. Users pass the card near a reader, and the reader reads the data from the card. Some access control points use proximity cards and pins for authentication.

### Monitoring Areas with Video Surveillance

Video surveillance provides reliable proof of a person's location and activity. It can record theft and track people. Many cameras include motion detection and object detection. CCTV systems can sometimes be a compensating control. 

### Sensors

Sensors monitor the environment and can detect change. Common sensors are noise and motion detection. Others include infrared, pressure, microwaves and ultrasonic waves.

## Adding Redundancy  and Fault Tolerance

### Single Point of Failure

A single point of failure is any component whose failure results in the failure of an entire system. RAID, load balancing, UPSes, and generators remove many single points of failure. RAID is an inexpensive method used to add fault tolerance and increase availability. A person being the only one who knows how to perform a task can be a single point of failure. 

### Disk Redundancies

RAID subsystems such as provide fault tolerance and increase availability. RAIND-1 and RAID-5 can survive the failure of one disk, and RAID-6 can survive the failure of two disks. RIAD-10 can survive more. 

### Server Redundancy 

Load balancing increases the overall power of a service by sharing the load between multiple servers. Configurations can be active/passive or active/active. Scheduling methods include round-robin and source IP address affinity. Source IP address affinity enforces clients to be redirected to the same server.

## Protecting Data with Backups

### Online vs. Offline Backups

If resources are not an issue, full backups provide the fastest recovery. Full/incremental strategies reduce the time needed to perform backups while saving some resources. Full/differential strategies reduce the amount needed to restore backups. 

### Business Impact Analysis Concepts 

A BIA identifies mission-essential functions and crucial systems. Essentially, what is most important in business resources. It also identifies maximum downtime limits for these systems and components, scenarios that could impact the systems (**Ex**. hurricanes), and potential losses. 

#### Recovery Time Objective and Recovery Point Objective

**RTO** identifies how long it should take to restore a system from an outage. It is derived from the BIA's maximum downtime limit. **RPO** refers to the amount of data you can afford to lose.

#### Mean Time Between Failures and Mean Time to Repair

**MBTF** provides a measure of a system's reliability and will provide how often a system might go down. **MTTR** refers to the time it takes to restore a system. 

### Continuity of Operations Planning 

A hot site is a backup site that is ready to go. A warm site may have pieces ready to go and need minimal resources to restore. A cold site is a site that is available and ready to set up. 

### Disaster Recovery

A **Disaster Recovery Plan** (**DRP**) identifies how to recover crucial systems when they go down. It also prioritizes services so restoration is as efficient as possible. The final phase of a DRP is lessons learned and potential updates. 

### Testing Plans with Exercises

You can validate business continuity plans with testing. Table-top exercises are discussions. Simulations are exactly that. Parallel processing activates a recovery while the primary site is running. Failover tests go through the process in real-time. They are the most dangerous and effective.

## References