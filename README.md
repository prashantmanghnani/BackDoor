# Back-door System

## Overview

The Back-door system is built upon two core concepts: Distributed Storage and Distributed Computing. It utilizes the Hadoop Distributed File System (HDFS) for storage and employs the MapReduce technique for distributed computing.

### Distributed Storage (HDFS)

#### Components

- **Namenode:** The master node that controls all network nodes.
- **Datanodes:** Worker nodes contributing storage space to the namenode, forming a virtual HDD.

#### Storage Process

1. **Virtual HDD Creation:** Datanodes allocate storage space to the namenode, creating a virtual HDD.
2. **Data Upload:** The namenode, interacting only with the client, showcases a storage space of 1-2TB. When a client uploads 200GB, the namenode breaks the data into blocks, storing each block on a datanode with 2-3 replications for fault tolerance.

### Distributed Computing (MapReduce)

#### Components

- **Jobtracker:** Coordinates tasks related to computation.
- **Tasktrackers:** Nodes connected to the jobtracker, responsible for task execution.

#### Computation Process

1. **Job Request:** When a client requests computation on stored data, the jobtracker contacts the namenode for datanode locations.
2. **Task Assignment:** Jobs are assigned to tasktrackers for parallel execution.

## Getting Started

### Prerequisites

- Hadoop must be installed and configured.
- Namenode and datanodes should be set up for distributed storage.
- Jobtracker and tasktrackers must be available for distributed computing.

### Usage

1. **Data Upload:**
   - Connect to the namenode for data storage.
   - Upload data, and the system handles distribution across datanodes.

2. **Computation:**
   - Request computation on stored data.
   - Jobtracker coordinates with the namenode to identify datanode locations.
   - Tasktrackers execute assigned computations in parallel.

## Contribution Guidelines

To contribute to the Back-door system:

1. Fork the repository.
2. Make your changes.
3. Submit a pull request.

Feel free to contact us for any questions or issues.
