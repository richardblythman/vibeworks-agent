# Stephen Dillon Demo Notes

## Background & Experience

Stephen has worked extensively in telecom optimization, starting at Vodafone where he built:
- Geolocation systems that ingested customer records to optimize network performance
- Data pipelines processing billions of data points daily
- Custom tools to work with binary files from network systems (no documentation available)

## Hackathon Project: Agentic RAN Optimization

Partnered with Kevin to tackle RAN (Radio Access Network) optimization at a hackathon. Used Claude to understand the domain ("I had no idea what a RAN network was") and accelerated development significantly.

Key insight: Claude enabled him to synthesize scattered knowledge and past work into production systems.

## Main Project: Fiber to the Home (FTTH) Network Tools

Stephen has been developing fiber network tools for 3-4 years. Built 5 core modules to address issues at companies like National Broadband Ireland:
- Antiquated systems
- Poor data quality
- Need for standardization and automation

### Core Modules

#### 1. **Fuse** - Alarm Aggregation Tool
- Builds fiber network as a graph (treats physical infrastructure as nodes/edges)
- Identifies break points in fiber network
- Aggregates multiple tickets down to single origin point
- Provides crucial context:
  - Downstream customer count affected
  - Network vulnerability metrics
  - Backhaul traffic information
- Enables engineers to prioritize repairs effectively (historically, engineers would chase false positives)

#### 2. **Pulses** - Anomaly Detection
- Detects anomalies at different network points
- Processes ~1 month of historical data
- Builds expected patterns and flags deviations
- Scores anomalies by ONU (Optical Network Unit - the broadband box)
- Helps determine if issues can be fixed remotely or require on-site visits

#### 3. **Upgrade Planning Tool**
- Recommends network upgrade locations based on budget constraints
- Incorporates multiple data factors:
  - Network vulnerabilities
  - Fiber infrastructure type (overhead vs. underground)
  - Environmental factors (tree foliage, wind speeds, etc.)
- Can also answer: "What investment required to reach X vulnerability threshold?"

#### 4. **Mapping/Query Generator Tool**
- Custom alternative to ArcGIS and MapInfo (which Stephen finds cumbersome)
- Includes extensive spatial functions (polygons, filtering, buffering, etc.)
- Query builder for complex geospatial operations
  - Example: buffer network layer by 100m, intersect with ONTs, find intersections
- Allows saving and exporting workflows
- Extremely flexible for ad-hoc analysis

#### 5. **Mirror** - Design Comparison Tool
- Compares high-level and low-level network designs
- Identifies differences between designs (extremely difficult problem normally)
- Previous manual approach: ~20 work days, €10,000 cost per 200km
- Current automated approach: ~20 minutes, near-zero cost (licensing only)
- Originally 100,000+ lines of code to build from scratch

## Technical Stack

- **Frontend**: React, MapGL, Recharts
- **Data Storage**: Graph DB
- **Streaming**: Kafka
- **Note**: Stephen isn't a traditional software engineer but has deep domain expertise

## How Claude Changed the Workflow

**Time savings**: Tasks that took 1-2 months now take 1 day

**Key enabler**: Pointing Claude to scattered past work and codebase
- Existing geospatial analytics codebase with solutions to complex problems
- Claude synthesizes documentation and context
- Enables rapid feature development by leveraging historical solutions

**Development timeline for main suite**: ~3 weeks (realistic estimate)

**Workflow pattern**:
1. Point Claude to problem domain and past code
2. Claude creates documentation of existing solutions
3. Identify opportunities to productize scattered knowledge
4. Rapidly build features by leveraging existing patterns

## Network Architecture Insights

### Fiber Networks (Graph-based)
- Built as directed graphs (nodes = infrastructure points, edges = fiber runs)
- Critical for understanding upstream/downstream impacts
- Many teams lack graph theory understanding - think point-to-point instead of end-to-end network comprehension

### RAN Networks (Geospatial)
- Subscriber geolocation + grid-based analysis
- Analyze overlapping cell coverage and signal strength
- Example: Built tool for HSE showing impact of cell outages on hospitals - some locations have redundancy, others are single points of failure

## Data Sources

### Fiber Network Data
- Feature sets from ArcGIS
- Fiber placement records, splice closure locations
- Requires network graph construction workflow

### RAN Network Data
- Binary trace files from network infrastructure
- Real-time and historical data sources
- May be C-feeds or files depending on network modernization level
- Must handle both modern and legacy systems

## Key Challenges Addressed

1. **Alarm fatigue** in networks (hundreds of alerts during storms)
2. **Prioritization** - optimizing crew dispatch to maximize impact
3. **Automation** - moving from reactive to proactive maintenance
4. **Lack of network understanding** - bridging gap between point-to-point and holistic end-to-end thinking
5. **Legacy system integration** - handling diverse data formats and systems

## Business Impact

- Massive cost reduction (€10,000 → near-zero for design comparison)
- Time savings (20 days → 20 minutes)
- Better decision-making through automated prioritization and anomaly detection
- Ability to prototype new features quickly from domain knowledge

