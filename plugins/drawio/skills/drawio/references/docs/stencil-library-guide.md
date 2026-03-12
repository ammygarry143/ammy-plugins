# Stencil Library Guide

Use semantic shapes by default. Switch to provider or device stencils only when the diagram needs vendor-specific meaning.

## Choose Semantic Shapes First

Use semantic shapes when:

- The diagram is conceptual or paper-facing.
- The audience cares more about function than vendor branding.
- You need strong theme consistency across the whole figure.

Use stencils when:

- The request explicitly mentions AWS, Azure, GCP, Cisco, Kubernetes, or other vendor/device families.
- The diagram is an engineering architecture or infrastructure reference.
- A provider icon materially improves clarity.

## Provider Prefixes

Common icon prefixes supported by the design system:

- `aws.*` → `mxgraph.aws4.*`
- `azure.*` → `mxgraph.azure.*`
- `gcp.*` → `mxgraph.gcp2.*`
- `k8s.*` → `mxgraph.kubernetes.*`

## Azure Stencil Reference

Azure uses `mxgraph.azure.*` shape names. The full verified catalog is in `design-system/icons.md`.

### Azure Color Palette

| Usage | Color |
|-------|-------|
| Primary fill | `#0078D4` (Azure blue) |
| Light fill | `#50E6FF` (Azure cyan) |
| Stroke | `none` (most icons) |
| Background group | `#EFF6FC` (light blue tint) |

### Azure mxCell Style Template

```xml
style="shape=mxgraph.azure.SHAPE_NAME;sketch=0;fillColor=#0078D4;strokeColor=none;
html=1;verticalLabelPosition=bottom;verticalAlign=top;align=center;outlineConnect=0;"
```

### Azure Service Group Container

Use a rounded rectangle with light blue fill to group services within the same Azure region or resource group:

```xml
<mxCell style="rounded=1;arcSize=4;fillColor=#EFF6FC;strokeColor=#0078D4;strokeWidth=2;
fontStyle=1;fontSize=11;verticalAlign=top;html=1;" vertex="1" parent="1">
  <mxGeometry x="40" y="40" width="400" height="280" as="geometry"/>
</mxCell>
```

### Important: No Guessing Shape Names

Only use Azure shape names verified from `design-system/icons.md`. Unrecognised `mxgraph.*` names silently render as plain coloured boxes. If a service is not in the verified list, either:
1. Use `shape=mxgraph.azure.cloud_service` as a generic Azure service placeholder.
2. Use a semantic shape with an Azure-blue fill.

## Rules

1. Do not guess stencil names — use only verified names from `design-system/icons.md`.
2. Keep label placement consistent (`verticalLabelPosition=bottom;verticalAlign=top`).
3. Always set `sketch=0` and `outlineConnect=0` to prevent rendering artefacts.
4. Azure: use `fillColor=#0078D4;strokeColor=none`. AWS: use service-specific colors. GCP: `fillColor=#4285F4`.
5. If mixed with semantic shapes, keep icon usage limited to nodes whose vendor identity matters.
6. In academic figures, prefer monochrome-compatible icons or add a legend.

## Recommended Usage

- Azure architecture: use `mxgraph.azure.*` icons; group by resource group using rounded containers.
- Cloud reference architecture: provider icons for gateways, queues, storage, compute.
- Network topology: device stencils for routers, switches, firewalls, APs.
- Academic/system paper figure: semantic shapes first; vendor icons only for external systems or deployment targets.
