<div align="center">

<a href="https://getunleash.io" title="Unleash - Empowering developers to release with confidence">
    <img src="./.github/github_header_opaque_landscape.svg" alt="Visit the Unleash website">
</a>

<br/>
<br/>

[![Build and Tests](https://img.shields.io/github/actions/workflow/status/Unleash/unleash/build.yaml?branch=main)](https://github.com/Unleash/unleash/actions/workflows/build.yaml) [![Coverage Status](https://coveralls.io/repos/github/Unleash/unleash/badge.svg?branch=main)](https://coveralls.io/github/Unleash/unleash?branch=main) [![Docker Pulls](https://img.shields.io/docker/pulls/unleashorg/unleash-server)](https://hub.docker.com/r/unleashorg/unleash-server) [![Apache-2.0 license](https://img.shields.io/github/license/unleash/unleash)](https://github.com/Unleash/unleash/blob/main/LICENSE) [![Join Unleash on Slack](https://img.shields.io/badge/slack-join-635dc5?logo=slack)](https://slack.unleash.run)

[Experience Unleash Live Demo →](https://www.getunleash.io/interactive-demo)

</div>

## What is Unleash?

* == feature management
  * powerful
  * 👀open-source 👀
* allows
  * development workflow,
    * == work | MULTIPLE features SIMULTANEOUSLY / NO need of separate feature branches 
  * accelerates software delivery,
  * controlling how & when roll out NEW features | end users 
  * deploying code | production / MORE manageable releases
* supports
  * 15 official client & server SDKs
  * \> 15 community SDKs

## Get started with Unleash

### Set up Unleash
#### Unleash Enterprise

* steps
  * [request a free trial](https://www.getunleash.io/plans/enterprise-payg?utm_source=oss&utm_medium=readme&utm_content=unleash-enterprise-start)
* free trial
  * == hosted instance / UNLIMITED 
    * projects & 
    * environments & 
    * features 
      * [role-based access control](https://docs.getunleash.io/reference/rbac),
      * [change requests](https://docs.getunleash.io/reference/change-requests),
      * [single sign-on](https://docs.getunleash.io/reference/sso),
      * [SCIM](https://docs.getunleash.io/reference/scim) -- for -- automatic user provisioning

#### Unleash Open Source

* open-source
* requirements
  * install 
    * [`git`](https://git-scm.com/)
    * [`docker`](https://www.docker.com/)
    * NodeJs
* ways
  * -- via -- docker
    * run
        ```bash
        git clone git@github.com:Unleash/unleash.git
        cd unleash
        docker compose up -d
        ```
    * | `localhost:4242`, log in -- via --
      ```
      username: `admin`
      password: `unleash4all`    
      ```
  * -- via -- NodeJs
    * see [step-by-step instructions](./CONTRIBUTING.md#how-to-run-the-project)

### Connect your SDK

* TODO:
Find your preferred SDK in [our list of official SDKs](#unleash-sdks) and import it into your project. Follow the setup guides for your specific SDK.

If you use the docker compose file from the previous step, here's the configuration details you'll need to get going:

- For front-end SDKs, use:
  - URL: `http://localhost:4242/api/frontend/`
  - `clientKey`: `default:development.unleash-insecure-frontend-api-token`
- For server-side SDKs, use:
  - Unleash API URL: `http://localhost:4242/api/`
  - API token: `default:development.unleash-insecure-api-token`

If you use a different setup, your configuration details will most likely also be different.

### Check a feature flag

Checking the state of a feature flag in your code is easy! The syntax will vary depending on your language, but all you need is a simple function call to check whether a flag is available. Here's how it might look in Java:

```java
if (unleash.isEnabled("AwesomeFeature")) {
  // do new, flashy thing
} else {
  // do old, boring stuff
}
```

### Run Unleash on a service?

If you don't want to run Unleash locally, we also provide easy deployment setups for Heroku and Digital Ocean:

[![Deploy to Heroku](./.github/deploy-heroku-20.png)](https://www.heroku.com/deploy/?template=https://github.com/Unleash/unleash) [![Deploy to DigitalOcean](./.github/deploy-digital.svg)](https://cloud.digitalocean.com/apps/new?repo=https://github.com/Unleash/unleash/tree/main&refcode=0e1d75187044)

### Configure and run Unleash anywhere

The above sections show you how to get up and running quickly and easily. When you're ready to start configuring and customizing Unleash for your own environment, check out the documentation for [getting started with self-managed deployments](https://docs.getunleash.io/reference/deploy/getting-started), [Unleash configuration options](https://docs.getunleash.io/reference/deploy/configuring-unleash), or [running Unleash locally via docker](https://docs.getunleash.io/tutorials/quickstart).

<br/>

## Online demo

* [Unleash online demo](https://www.getunleash.io/interactive-demo)

## Community

* [Slack](https://slack.unleash.run)

## How to contribute?

* see
  * [CONTRIBUTING.md file](./CONTRIBUTING.md)
  * [Unleash developer guideliness](./website/docs/contributing/developer-guide.md)

## Features our users love

### Flexibility and adaptability

- Get an overview of all feature flags across all your environments, applications and services
- Targeted releases using [activation strategies](https://docs.getunleash.io/reference/activation-strategies) to enable and disable features for certain users or segments without having to redeploy your application.
- [Canary releases / gradual rollouts](https://docs.getunleash.io/reference/activation-strategies#gradual-rollout)
- [Kill switches](https://docs.getunleash.io/reference/feature-toggles#feature-flag-types)
- [A/B testing](https://docs.getunleash.io/feature-flag-tutorials/use-cases/a-b-testing)
- 2 [environments](https://docs.getunleash.io/reference/environments)
- Organize feature flags using [tags](https://docs.getunleash.io/reference/feature-toggles#tags)
- Out-of-the-box integrations with popular tools ([Slack](https://docs.getunleash.io/addons/slack), [Microsoft Teams](https://docs.getunleash.io/addons/teams), [Datadog](https://docs.getunleash.io/addons/datadog)) + integrate with anything with [webhooks](https://docs.getunleash.io/addons/webhook)
- [Insights for managing technical debt](https://docs.getunleash.io/reference/technical-debt) and [stale flags](https://docs.getunleash.io/reference/technical-debt#stale-and-potentially-stale-flags)
- API-first: _everything_ can be automated. No exceptions.
- [12 official client SDKs](https://docs.getunleash.io/reference/sdks#official-sdks), and 10 [community-contributed client SDKs](https://docs.getunleash.io/reference/sdks#community-sdks)
- Run it via Docker with the [official Docker image](https://hub.docker.com/r/unleashorg/unleash-server) or as a pure Node.js application

### Security and performance

- Privacy by design (GDPR and Schrems II). End-user data never leaves your application.
- [Audit logs](https://docs.getunleash.io/advanced/audit_log)
- Enforce [OWASP's secure headers](https://owasp.org/www-project-secure-headers/) via the strict HTTPS-only mode
- Flexible hosting options: host it on premise or in the cloud (_any_ cloud)
- Scale with [Unleash Edge](https://docs.getunleash.io/reference/unleash-edge) independently of the Unleash server to support any number of front-end clients without overloading your Unleash instance

### Looking for more features?

If you're looking for one of the following features, please take a look at our [Pro and Enterprise plans](https://www.getunleash.io/plans):

- [role-based access control (RBAC)](https://docs.getunleash.io/reference/rbac)
- [single sign-on (SSO)](https://docs.getunleash.io/reference/sso)
- more environments
- [feature flags project support](https://docs.getunleash.io/reference/projects)
- [advanced segmentation](https://docs.getunleash.io/reference/segments)
- [additional strategy constraints](https://docs.getunleash.io/reference/activation-strategies#constraints)
- tighter security
- more hosting options (we can even host it for you!)

<br/>

## Architecture

<img src="./website/static/img/unleash-architecture-edge.png" title="Unleash System Overview" />

Read more in the [_system overview_ section of the Unleash documentation](https://docs.getunleash.io/understanding-unleash/unleash-overview#system-overview).

<br/>

## Unleash SDKs

To connect your application to Unleash you'll need to use a client SDK for your programming language.

**Official server-side SDKs:**

- [Go SDK](https://docs.getunleash.io/reference/sdks/go)
- [Java SDK](https://docs.getunleash.io/reference/sdks/java)
- [Node.js SDK](https://docs.getunleash.io/reference/sdks/node)
- [PHP SDK](https://docs.getunleash.io/reference/sdks/php)
- [Python SDK](https://docs.getunleash.io/reference/sdks/python)
- [Ruby SDK](https://docs.getunleash.io/reference/sdks/ruby)
- [Rust SDK](https://github.com/unleash/unleash-client-rust)
- [.NET SDK](https://docs.getunleash.io/reference/sdks/dotnet)

**Official front-end SDKs:**

The front-end SDKs connect via [Unleash Edge](https://docs.getunleash.io/reference/unleash-edge) in order to ensure privacy, scalability and security.

- [Android Proxy SDK](https://docs.getunleash.io/reference/sdks/android-proxy)
- [Flutter Proxy SDK](https://docs.getunleash.io/reference/sdks/flutter)
- [iOS Proxy SDK](https://docs.getunleash.io/reference/sdks/ios-proxy)
- [JavaScript Proxy SDK](https://docs.getunleash.io/reference/sdks/javascript-browser)
- [React Proxy SDK](https://docs.getunleash.io/reference/sdks/react)
- [Svelte Proxy SDK](https://docs.getunleash.io/reference/sdks/svelte)
- [Vue Proxy SDK](https://docs.getunleash.io/reference/sdks/vue)

**Community SDKs:**

If none of the official SDKs fit your need, there's also a number of [community-developed SDKs](https://docs.getunleash.io/reference/sdks#community-sdks) where you might find an implementation for your preferred language (such as [Elixir](https://gitlab.com/afontaine/unleash_ex), [Dart](https://pub.dev/packages/unleash), [Clojure](https://github.com/AppsFlyer/unleash-client-clojure), and more).

<br/>

## Users of Unleash

**Unleash is trusted by thousands of companies all over the world**.

**Proud Open-Source users:** (send us a message if you want to add your logo here)

![The Unleash logo encircled by logos for Finn.no, nav (the Norwegian Labour and Welfare Administration), Budgets, Otovo, and Amedia. The encircling logos are all connected to the Unleash logo.](./.github/github_unleash_users.svg)

<br/>

## Migration guides

Unleash has evolved significantly over the past few years, and we know how hard it can be to keep software up to date. If you're using the current major version, upgrading shouldn't be an issue. If you're on a previous major version, check out the [Unleash migration guide](https://docs.getunleash.io/deploy/migration_guide)!

<br/>

## Want to know more about Unleash?

### Videos and podcasts

- [The Unleash YouTube channel](https://www.youtube.com/channel/UCJjGVOc5QBbEje-r7nZEa4A)
- [_Feature toggles — Why and how to add to your software_ — freeCodeCamp (YouTube)](https://www.youtube.com/watch?v=-yHZ9uLVSp4&t=0s)
- [_Feature flags with Unleash_ — The Code Kitchen (podcast)](https://share.fireside.fm/episode/zD-4e4KI+Pr379KBv)
- [_Feature Flags og Unleash med Fredrik Oseberg_ — Utviklerpodden (podcast; Norwegian)](https://pod.space/utviklerpodden/feature-flags-og-unleash-med-fredrik-oseberg)

### Articles and more

- [The Unleash Blog](https://www.getunleash.io/blog)
- [_Designing the Rust Unleash API client_ — Medium](https://medium.com/cognite/designing-the-rust-unleash-api-client-6809c95aa568)
- [_FeatureToggle_ by Martin Fowler](http://martinfowler.com/bliki/FeatureToggle.html)
- [_Feature toggling transient errors in load tests_ — nrkbeta](https://nrkbeta.no/2021/08/23/feature-toggling-transient-errors-in-load-tests/)
- [_An Interview with Ivar of Unleash_ — Console](https://console.substack.com/p/console-42)
- [_Unleash your features gradually_](http://ivarconr.github.io/feature-toggles-presentation/sch-dev-lunch-2017/#1 ' '), slideshow/presentation by Ivar, the creator of Unleash
