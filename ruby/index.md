title: Ruby Development on Cloud Foundry

!SLIDE

<%= include "../shared/monica.md" %>

!SLIDE

<%= include "../shared/intro_paas.md" %>

!SLIDE

<%= include "../shared/vmc.md" %>

!SLIDE

<%= include "../shared/micro.md" %>

!SLIDE

## Ruby Support

### Runtimes
- Ruby 1.8.7
- Ruby 1.9.2

### Frameworks
- Sinatra
- Rails

!SLIDE

## New framework Support
- Rails 3.1 and 3.2 applications are now well-supported on CloudFoundry.com. 
- JRuby
- Rack Applications - Applications written with Rack, a modular Ruby web server interface, are now supported. 
  - Cloud Foundry's VMC will automatically recognize a config.ru Rackup file and use it to run your web application. 
  - The auto-reconfiguration feature is also supported for rack applications

!SLIDE

## Services

- MySQL 5.1
- PostgreSQL 9.0
- MongoDB 1.8
- Redis 2.2
- RabbitMQ 2.4

!SLIDE

## Auto Reconfiguration

Until this feature was released, ruby developers had to add code to read at runtime the credentials for each service.

Gems like [cloudfoundry-env](https://github.com/cloudfoundry-samples/cloudfoundry-env) helped with this task but now thanks to code injection
All connections against localhost are modified to access the proper service

**It just works**

!SLIDE

## Service tunneling

- The ability to access any service on Cloud Foundry as if it was running locally


    gem install caldecott

    vmc tunnel [service_name]


TODO: Add MongoHub Screenshot

!SLIDE

## Rails Console


    vmc rails-console [appname]

- Requires 0.3.16.beta.3 or higher.

TODO: Add screenshot

!SLIDE

<%= include "../shared/standalone.md" %>

!SLIDE

<%= include "../shared/manifest.md" %>





