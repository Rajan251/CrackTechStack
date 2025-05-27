
## Topic 1: AWS Service Naming Convention

### Amazon Services vs AWS Services (Within AWS Cloud)

#### Amazon Services (Core Infrastructure)
- **Amazon S3** - Simple Storage Service (file storage)
- **Amazon EC2** - Elastic Compute Cloud (virtual machines)
- **Amazon RDS** - Relational Database Service (managed databases)
- **Amazon Lambda** - Serverless compute functions
- **Amazon VPC** - Virtual Private Cloud (networking)
- **Amazon CloudFront** - Content Delivery Network (CDN)
- **Amazon DynamoDB** - NoSQL database
- **Amazon EBS** - Elastic Block Store (disk storage)

#### AWS Services (Management & Supporting Tools)
- **AWS IAM** - Identity and Access Management (user permissions)
- **AWS CloudFormation** - Infrastructure as Code (automated setup)
- **AWS CloudWatch** - Monitoring and logging service
- **AWS Config** - Configuration management
- **AWS CloudTrail** - API activity logging
- **AWS Systems Manager** - System administration tools
- **AWS Organizations** - Multi-account management
- **AWS Cost Explorer** - Cost analysis tool

#### Naming Rule
- **Amazon** = Core compute, storage, and database services (fundamental building blocks)
- **AWS** = Management, monitoring, and configuration services (tools to manage Amazon services)

---

## Topic 2: Scaling Concepts

### Vertical Scaling (Up/Down)

#### Scale Up (Vertical Scale Up)
- **Definition**: Increase resources of existing server
- **What changes**: CPU, RAM, storage capacity of same machine
- **Example**: Upgrade EC2 instance from t2.micro (1GB RAM) to t2.large (8GB RAM)
- **When to use**: Single application needs more power
- **Pros**: Simple, no code changes needed
- **Cons**: Limited by hardware limits, single point of failure

#### Scale Down (Vertical Scale Down)
- **Definition**: Decrease resources of existing server
- **What changes**: Reduce CPU, RAM, storage of same machine
- **Example**: Downgrade EC2 instance from t2.large (8GB RAM) to t2.small (2GB RAM)
- **When to use**: Over-provisioned resources, cost optimization
- **Benefit**: Cost savings

### Horizontal Scaling (Out/In)

#### Scale Out (Horizontal Scale Out)
- **Definition**: Add more servers/instances
- **What changes**: Number of machines increases
- **Example**: Go from 1 EC2 instance to 5 EC2 instances
- **When to use**: High traffic, need redundancy
- **Pros**: Better fault tolerance, can handle massive loads
- **Cons**: More complex, may need code changes

#### Scale In (Horizontal Scale In)
- **Definition**: Remove servers/instances
- **What changes**: Number of machines decreases
- **Example**: Go from 10 EC2 instances to 3 EC2 instances
- **When to use**: Traffic decreased, cost optimization
- **Benefit**: Cost savings, simplified management

### Quick Memory Aid

| Direction | Vertical (Server Power) | Horizontal (Server Count) |
|-----------|------------------------|---------------------------|
| **Increase** | Scale UP ⬆️ (More power) | Scale OUT ➡️ (More servers) |
| **Decrease** | Scale DOWN ⬇️ (Less power) | Scale IN ⬅️ (Fewer servers) |

### Real-World Example
**Scenario**: Your e-commerce website is running slow during Black Friday

**Options**:
1. **Scale Up**: Upgrade your single server from 4GB to 16GB RAM
2. **Scale Out**: Keep 4GB servers but add 4 more servers (total 5 servers)
3. **Both**: Upgrade to 8GB servers AND add more servers

**Best Practice**: Use Scale Out for better reliability (if one server fails, others continue working)
