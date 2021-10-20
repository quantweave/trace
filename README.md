## Evaluation of tracing applications

### Requirements
 - deployable in cloud
 - collect traces with trace id
 - collect payload from request/response

### Candidates
 - [trasier](https://github.com/trasiercom)
 - [hypertrace](https://github.com/hypertrace)
 - [apm](https://github.com/elastic/apm-server)

### Findings

#### Trasier
- Missing UI that has to be build in Backstage
- Requires keycloak realm for token OAUTH2 
#### Hypertrace
- Requires large infrastructure
#### APM
- Records only requests body not responses [link](https://discuss.elastic.co/t/apm-capture-response-body/249990)