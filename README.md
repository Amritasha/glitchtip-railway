# Deploy and Host GlitchTip on Railway

GlitchTip is an open-source error tracking and performance monitoring platform. It collects, groups, and alerts on application errors using Sentry-compatible SDKs — giving you a fully self-hosted alternative to Sentry with complete data ownership and no per-event pricing surprises.

## About Hosting GlitchTip

Hosting GlitchTip requires running its Django-based application server alongside PostgreSQL for data storage and Redis for caching and background task processing. GlitchTip uses Celery workers to process incoming error events asynchronously, so the worker process must run alongside the web server. On Railway, all services — web, worker, Postgres, and Redis — can be deployed within the same project and networked automatically. You will also need an SMTP provider configured for alert notifications and user account emails.

## Common Use Cases

- Tracking and triaging application errors across multiple projects and environments
- Replacing Sentry with a self-hosted solution to keep error data private and costs predictable
- Monitoring uptime and performance for production web services with team alerting

## Dependencies for GlitchTip Hosting

- **PostgreSQL** — primary store for error events, projects, teams, and alert configurations
- **Redis** — task queue backend for Celery workers processing incoming error events

### Deployment Dependencies

- [GlitchTip Documentation](https://glitchtip.com/documentation)
- [GlitchTip GitLab Repository](https://gitlab.com/glitchtip/glitchtip-backend)
- [GlitchTip Self-Hosting Guide](https://glitchtip.com/documentation/install)
- [Railway PostgreSQL Plugin](https://docs.railway.com/databases/postgresql)
- [Railway Redis Plugin](https://docs.railway.com/databases/redis)

## Why Deploy GlitchTip on Railway?

Railway is a singular platform to deploy your infrastructure stack. Railway will host your infrastructure so you do not have to deal with configuration, while allowing you to vertically and horizontally scale it.

By deploying GlitchTip on Railway, you are one step closer to supporting a complete full-stack application with minimal burden. Host your servers, databases, AI agents, and more on Railway.
