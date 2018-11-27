# What to do when failure detected?
- Stop?
-- Sometimes this is right --> Unauthenticated user detected -- stop everything
- Carry on?

# Good teams practice failure often.
- Application wide
- Datacenter wide

# Famous Error recently:
- Re-register domain
- Certificate Failures
- Disaster: Hurricanes

Book to read: Release it! By Michael Nygard

__DEF: Chaos Enginneering == Experiment to ensure that the impact of failure is mitigated__

Key Questions:
1. What went wrong?
2. What did we not expect?

# Taxonomy
- Operations
- Application
- Software Stack
- Infrastructure

# First Steps
White board based upon taxonomy
White board based upon state
Build Chaos from the Beginning
Establish Hypothesis


Timeline
- Disaster Recovery
-- Focus on batch recovery
-- RPO = Recovery Point Objective -> interval between backup
-- RTO = Recovery Time Objective -> interval to get recover
- Institute Chaos Eng.
-- 
- Resilient Critical Systems

# Layers 
- People -> Experience Staff through Game Days
- Applications -> Robust Apps
- Switching 
- Infrastructure

Reliability = Frequency of Test x Availability 

# Adversarial Teams
- Security & Chaos should be one team 
- Infrastructure team

# AWS Isolation Model
Availability are close enough to do synchronous replication.
Mechanisms:
- Modify IAM roles -- Drop IAM permissions by VPC or Region

# Types of attacks
- Resource
- Network
- State
-- Host
-- Container / Application

# Hypothesis makeup
- Form hypothesis
- Run an experiment
- Abort Conditions
-- Define blast radius --> Start Small
-- Consider SLA/SLO
- Define Success & Failure
- Fix Fix Fix

# Chaos Engineering & Monitoring
Part of hypothesis should include what monitors should show


[Community Site] (http://gremlin.com/community)
[Slack Channel] (http://bit.ly/chaos-eng-slack)

# Observability & Isolation
- High -> Functions
- Medium -> Micro-services, Monolith with Tracing and Logging
- Low -> Monolith with no logging 

# Epidemic Failure
- EX: Linux Leap Second bug --> Quarantine with Running Windows (Ugh)
- EX: Zone or Region Failure --> Cross Zone or Region Repl
- EX: DNS Failure --> Multiple domains and providers
- EX: Syntax Error --> DHH: Linting is critical to protect this --> Limit Scope of Deployment

Chaos Engineering Tip: Follow SRE Moto -> "If it's painful, do it often"

