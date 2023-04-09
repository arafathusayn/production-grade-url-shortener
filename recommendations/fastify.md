### Recommendations for Fastify

- **TypeScript**: Use it to avoid type-level errors at compile-time.
- **Authentication**: Use [Passport.js](https://github.com/fastify/fastify-passport) strategies. Sessions should be stored in an external database so that it can support a load-balanced system.
- **Authorization in a persistent database**: There are many options to implement this. You may implement your own role-permission tables in a [Postgres](https://github.com/fastify/fastify-postgres) database. You may use an ORM to speed things up like [Prisma](https://github.com/prisma/prisma) and [TypeORM](https://github.com/typeorm/typeorm). Use database-pooling and atomic transactions. Alternatively, you may use hosted services which provide distributed and serverless databases like [Planetscale](https://planetscale.com/) or [CockroachDB](https://www.cockroachlabs.com/).
- **URL Expiration**: Use Cron Jobs with [BullMQ](https://github.com/taskforcesh/bullmq) and [Bull Board](https://github.com/felixmosh/bull-board) for UI.
- **Rate Limit**: Use [Fastify Rate Limit](https://github.com/fastify/fastify-rate-limit) for windowed rate limit.
- **Logging**: Use [Pino](https://www.fastify.io/docs/latest/Reference/Logging/)
- **OpenAPI Spec**: Auto-generate [Docs](https://github.com/ShogunPanda/fastify-openapi-docs)
- **Validation**: Fastify has support for [JSON Schema](https://www.fastify.io/docs/latest/Guides/Fluent-Schema/).
- **Security**:
    - [Helmet](https://github.com/fastify/fastify-helmet)
    - [CORS](https://github.com/fastify/fastify-cors)
    - [CSRF protection](https://github.com/fastify/csrf-protection)
    - [Let's Encrypt](https://letsencrypt.org/getting-started/)
- **Caching**:
    - [Redis](https://github.com/fastify/fastify-redis)
- **Automated Testing**:
    - [Tap](https://node-tap.org/docs/getting-started/) is recommended in the official [Fastify CLI](https://github.com/fastify/fastify-cli)