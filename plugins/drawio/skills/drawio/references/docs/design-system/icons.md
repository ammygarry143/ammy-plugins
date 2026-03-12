# Icon Libraries

The Design System provides integration with cloud provider icons and technical symbols for professional architecture diagrams.

---

## Cloud Provider Icons

### AWS (Amazon Web Services)

Icons use the `mxgraph.aws4.*` shape prefix.

#### Compute

| Service | Icon Reference | Shape |
|---------|---------------|-------|
| Lambda | `aws.lambda` | `mxgraph.aws4.lambda` |
| EC2 | `aws.ec2` | `mxgraph.aws4.ec2` |
| ECS | `aws.ecs` | `mxgraph.aws4.ecs` |
| EKS | `aws.eks` | `mxgraph.aws4.eks` |
| Fargate | `aws.fargate` | `mxgraph.aws4.fargate` |

#### Storage & Database

| Service | Icon Reference | Shape |
|---------|---------------|-------|
| S3 | `aws.s3` | `mxgraph.aws4.s3` |
| DynamoDB | `aws.dynamodb` | `mxgraph.aws4.dynamodb` |
| RDS | `aws.rds` | `mxgraph.aws4.rds` |
| ElastiCache | `aws.elasticache` | `mxgraph.aws4.elasticache` |

#### Networking

| Service | Icon Reference | Shape |
|---------|---------------|-------|
| API Gateway | `aws.api-gateway` | `mxgraph.aws4.api_gateway` |
| CloudFront | `aws.cloudfront` | `mxgraph.aws4.cloudfront` |
| Route 53 | `aws.route53` | `mxgraph.aws4.route_53` |
| VPC | `aws.vpc` | `mxgraph.aws4.vpc` |
| ALB | `aws.alb` | `mxgraph.aws4.application_load_balancer` |

#### Integration

| Service | Icon Reference | Shape |
|---------|---------------|-------|
| SQS | `aws.sqs` | `mxgraph.aws4.sqs` |
| SNS | `aws.sns` | `mxgraph.aws4.sns` |
| EventBridge | `aws.eventbridge` | `mxgraph.aws4.eventbridge` |
| Step Functions | `aws.step-functions` | `mxgraph.aws4.step_functions` |

---

### GCP (Google Cloud Platform)

Icons use the `mxgraph.gcp2.*` shape prefix.

#### Compute

| Service | Icon Reference | Shape |
|---------|---------------|-------|
| Cloud Run | `gcp.cloud-run` | `mxgraph.gcp2.cloud_run` |
| Cloud Functions | `gcp.functions` | `mxgraph.gcp2.cloud_functions` |
| Compute Engine | `gcp.compute` | `mxgraph.gcp2.compute_engine` |
| GKE | `gcp.gke` | `mxgraph.gcp2.kubernetes_engine` |

#### Storage & Database

| Service | Icon Reference | Shape |
|---------|---------------|-------|
| Cloud Storage | `gcp.storage` | `mxgraph.gcp2.cloud_storage` |
| Cloud SQL | `gcp.sql` | `mxgraph.gcp2.cloud_sql` |
| Firestore | `gcp.firestore` | `mxgraph.gcp2.firestore` |
| BigQuery | `gcp.bigquery` | `mxgraph.gcp2.bigquery` |

#### Networking

| Service | Icon Reference | Shape |
|---------|---------------|-------|
| Cloud Load Balancing | `gcp.lb` | `mxgraph.gcp2.cloud_load_balancing` |
| Cloud CDN | `gcp.cdn` | `mxgraph.gcp2.cloud_cdn` |
| Cloud DNS | `gcp.dns` | `mxgraph.gcp2.cloud_dns` |

---

### Azure (Microsoft Azure)

Icons use the `mxgraph.azure.*` shape prefix. Azure brand color: `#0078D4` (blue). Use `strokeColor=none` for clean rendering.

#### Azure mxCell Style Template

```xml
<mxCell style="shape=mxgraph.azure.SHAPE_NAME;sketch=0;fillColor=#0078D4;strokeColor=none;html=1;verticalLabelPosition=bottom;verticalAlign=top;align=center;outlineConnect=0;"
  vertex="1" parent="1">
  <mxGeometry width="60" height="60" as="geometry"/>
</mxCell>
```

#### Platform & Identity

| Service | Icon Reference | Shape |
|---------|---------------|-------|
| Azure Logo | `azure.azure` | `mxgraph.azure.azure` |
| Active Directory | `azure.active-directory` | `mxgraph.azure.active_directory` |
| Azure AD | `azure.azure-ad` | `mxgraph.azure.azure_active_directory` |
| Key Vault | `azure.key-vault` | `mxgraph.azure.key_vault` |
| Monitor | `azure.monitor` | `mxgraph.azure.monitor` |
| Automation | `azure.automation` | `mxgraph.azure.automation` |
| Operational Insights | `azure.log-analytics` | `mxgraph.azure.operational_insights` |
| Alert | `azure.alert` | `mxgraph.azure.alert` |
| SDK | `azure.sdk` | `mxgraph.azure.sdk` |

#### Compute

| Service | Icon Reference | Shape |
|---------|---------------|-------|
| Virtual Machine | `azure.vm` | `mxgraph.azure.virtual_machine` |
| App Service | `azure.app-service` | `mxgraph.azure.app_services` |
| Functions | `azure.functions` | `mxgraph.azure.functions` |
| AKS | `azure.aks` | `mxgraph.azure.kubernetes_services` |
| Batch | `azure.batch` | `mxgraph.azure.batch` |
| Service Fabric | `azure.service-fabric` | `mxgraph.azure.service_fabric` |
| Cloud Service | `azure.cloud-service` | `mxgraph.azure.cloud_service` |
| Web Roles | `azure.web-roles` | `mxgraph.azure.web_roles` |
| Worker Roles | `azure.worker-roles` | `mxgraph.azure.worker_roles` |
| Remote App | `azure.remote-app` | `mxgraph.azure.remote_app` |
| Mobile Services | `azure.mobile` | `mxgraph.azure.mobile_services` |
| Media Services | `azure.media` | `mxgraph.azure.media_services` |

#### Storage

| Service | Icon Reference | Shape |
|---------|---------------|-------|
| Storage | `azure.storage` | `mxgraph.azure.storage` |
| Blob Storage | `azure.blob` | `mxgraph.azure.blob_storage` |
| Queue Storage | `azure.queue-storage` | `mxgraph.azure.queue_storage` |
| Table Storage | `azure.table-storage` | `mxgraph.azure.table_storage` |
| Data Lake Store | `azure.data-lake-store` | `mxgraph.azure.data_lake_store` |

#### Databases

| Service | Icon Reference | Shape |
|---------|---------------|-------|
| SQL Database | `azure.sql` | `mxgraph.azure.sql_database` |
| SQL Server | `azure.sql-server` | `mxgraph.azure.sql_server` |
| SQL Stretch DB | `azure.sql-stretch` | `mxgraph.azure.sql_stretch_database` |
| Cosmos DB | `azure.cosmos` | `mxgraph.azure.cosmos_db` |
| Redis Cache | `azure.redis` | `mxgraph.azure.redis_cache` |
| HDInsight | `azure.hdinsight` | `mxgraph.azure.hdinsight` |

#### Networking

| Service | Icon Reference | Shape |
|---------|---------------|-------|
| Virtual Network | `azure.vnet` | `mxgraph.azure.virtual_network` |
| VPN Gateway | `azure.vpn` | `mxgraph.azure.vpn_gateway` |
| ExpressRoute | `azure.expressroute` | `mxgraph.azure.express_route` |
| Load Balancer | `azure.lb` | `mxgraph.azure.load_balancer` |
| Application Gateway | `azure.app-gateway` | `mxgraph.azure.application_gateway` |
| Traffic Manager | `azure.traffic-manager` | `mxgraph.azure.traffic_manager` |
| CDN | `azure.cdn` | `mxgraph.azure.cdn` |
| DNS | `azure.dns` | `mxgraph.azure.dns` |

#### Integration & Messaging

| Service | Icon Reference | Shape |
|---------|---------------|-------|
| Service Bus | `azure.service-bus` | `mxgraph.azure.service_bus` |
| Event Hubs | `azure.event-hubs` | `mxgraph.azure.event_hubs` |
| Notification Hubs | `azure.notification-hub` | `mxgraph.azure.notification_hub` |
| BizTalk Services | `azure.biztalk` | `mxgraph.azure.biztalk_services` |
| Scheduler | `azure.scheduler` | `mxgraph.azure.scheduler` |
| API Management | `azure.apim` | `mxgraph.azure.api_management` |
| Logic App | `azure.logic-app` | `mxgraph.azure.app_service_logic_app` |

#### Analytics & AI

| Service | Icon Reference | Shape |
|---------|---------------|-------|
| Machine Learning | `azure.ml` | `mxgraph.azure.machine_learning` |
| Data Factory | `azure.data-factory` | `mxgraph.azure.data_factory` |
| Data Lake Analytics | `azure.data-lake-analytics` | `mxgraph.azure.data_lake_analytics` |
| Stream Analytics | `azure.stream-analytics` | `mxgraph.azure.stream_analytics` |
| Azure Search | `azure.search` | `mxgraph.azure.search` |
| Cognitive Services | `azure.cognitive` | `mxgraph.azure.cognitive_services` |
| IoT Hub | `azure.iot-hub` | `mxgraph.azure.iot_hub` |

---

## DevOps Icons

### Container & Orchestration

| Tool | Icon Reference | Shape |
|------|---------------|-------|
| Docker | `devops.docker` | `mxgraph.docker.docker` |
| Kubernetes | `devops.kubernetes` | `mxgraph.kubernetes.kubernetes` |
| Helm | `devops.helm` | Custom SVG |

### CI/CD

| Tool | Icon Reference | Shape |
|------|---------------|-------|
| GitHub Actions | `devops.github-actions` | Custom SVG |
| Jenkins | `devops.jenkins` | Custom SVG |
| GitLab CI | `devops.gitlab` | Custom SVG |
| ArgoCD | `devops.argocd` | Custom SVG |

---

## ML/AI Icons

### Neural Network Symbols

| Symbol | Icon Reference | Description |
|--------|---------------|-------------|
| Input Layer | `ml.input` | Circle with arrows in |
| Hidden Layer | `ml.hidden` | Stacked circles |
| Output Layer | `ml.output` | Circle with arrows out |
| Convolution | `ml.conv` | Grid pattern |
| Pooling | `ml.pool` | Shrinking grid |

### Data Pipeline

| Symbol | Icon Reference | Description |
|--------|---------------|-------------|
| Data Source | `ml.data-source` | Database with arrow |
| Transform | `ml.transform` | Gears |
| Model | `ml.model` | Brain/network icon |
| Prediction | `ml.predict` | Target/bullseye |

---

## Usage

### In Specification

```yaml
nodes:
  - id: lambda
    label: Order Handler
    icon: aws.lambda
    
  - id: db
    label: Orders DB
    icon: aws.dynamodb
```

### Icon Normalization

The system normalizes common variations:

| User Input | Resolved To |
|------------|-------------|
| `api-gateway` | `mxgraph.aws4.api_gateway` |
| `lambda` | `mxgraph.aws4.lambda` |
| `s3` | `mxgraph.aws4.s3` |
| `cloud-run` | `mxgraph.gcp2.cloud_run` |

### Icon with Custom Size

```yaml
nodes:
  - id: logo
    label: AWS Lambda
    icon: aws.lambda
    size: large  # 160×80 px with icon
```

---

## mxCell Style for Icons

```xml
<mxCell style="shape=mxgraph.aws4.lambda;
  verticalLabelPosition=bottom;align=center;
  outlineConnect=0;dashed=0;verticalAlign=top;
  fillColor=#F58536;strokeColor=#ffffff;
  html=1;" />
```

Key properties:

- `shape`: Icon shape reference
- `verticalLabelPosition`: Label below icon (`bottom`)
- `fillColor`: Icon fill (AWS orange for Lambda)

---

## Best Practices

### Consistency

- Use same cloud provider icons throughout diagram
- Don't mix AWS and GCP icons unless showing multi-cloud

### Labeling

- Place labels below icons
- Keep labels short (service name only)
- Use tooltips for additional details

### Size

- Standard icon size: 60×60 px
- With label: 80×90 px total
- Keep icons same size for visual balance

### Grouping

- Group related services in modules
- Use consistent spacing (32px between icons)
- Align icons to 8px grid

---

## Adding Custom Icons

For icons not in built-in libraries:

1. **Use SVG**: Import SVG as custom shape
2. **Use Image**: Embed as base64 image
3. **Use stencil**: Reference draw.io stencil library

```yaml
nodes:
  - id: custom
    label: Custom Service
    style:
      image: "data:image/svg+xml,..."
      shape: image
```
