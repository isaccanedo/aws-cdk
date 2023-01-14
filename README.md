# AWS Cloud Development Kit (AWS CDK)

![Build Status](https://codebuild.us-east-1.amazonaws.com/badges?uuid=eyJlbmNyeXB0ZWREYXRhIjoiSy9rWmVENzRDbXBoVlhYaHBsNks4OGJDRXFtV1IySmhCVjJoaytDU2dtVWhhVys3NS9Odk5DbC9lR2JUTkRvSWlHSXZrNVhYQ3ZsaUJFY3o4OERQY1pnPSIsIml2UGFyYW1ldGVyU3BlYyI6IlB3ODEyRW9KdU0yaEp6NDkiLCJtYXRlcmlhbFNldFNlcmlhbCI6MX0%3D&branch=master)
[![Gitpod Ready-to-Code](https://img.shields.io/badge/Gitpod-ready--to--code-blue?logo=gitpod)](https://gitpod.io/#https://github.com/aws/aws-cdk)
[![NPM version](https://badge.fury.io/js/aws-cdk.svg)](https://badge.fury.io/js/aws-cdk)
[![PyPI version](https://badge.fury.io/py/aws-cdk.core.svg)](https://badge.fury.io/py/aws-cdk.core)
[![NuGet version](https://badge.fury.io/nu/Amazon.CDK.svg)](https://badge.fury.io/nu/Amazon.CDK)
[![Maven Central](https://maven-badges.herokuapp.com/maven-central/software.amazon.awscdk/core/badge.svg)](https://maven-badges.herokuapp.com/maven-central/software.amazon.awscdk/core)
[![Go Reference](https://pkg.go.dev/badge/github.com/aws/aws-cdk-go/awscdk.svg)](https://pkg.go.dev/github.com/aws/aws-cdk-go/awscdk)
[![Mergify](https://img.shields.io/endpoint.svg?url=https://gh.mergify.io/badges/aws/aws-cdk&style=flat)](https://mergify.io)

O **AWS Cloud Development Kit (AWS CDK)** é uma estrutura de desenvolvimento de 
software de código aberto para definir a infraestrutura de nuvem em código e provisioná-la por meio do AWS CloudFormation.

Ele oferece uma abstração orientada a objetos de alto nível para definir os recursos da AWS 
de forma imperativa usando o poder das linguagens de programação modernas.Usando a biblioteca 
de construções de infraestrutura do CDK, você pode facilmente encapsular as melhores práticas da AWS em sua 
definição de infraestrutura e compartilhá-la sem se preocupar com a lógica clichê.

O CDK está disponível nos seguintes idiomas:

* JavaScript, TypeScript ([Node.js ≥ 10.13.0](https://nodejs.org/download/release/latest-v10.x/))
  - We recommend using a version in [Active LTS](https://nodejs.org/en/about/releases/)
  - ⚠️ versions `13.0.0` to `13.6.0` are not supported due to compatibility issues with our dependencies.
* Python ([Python ≥ 3.6](https://www.python.org/downloads/))
* Java ([Java ≥ 8](https://www.oracle.com/technetwork/java/javase/downloads/index.html) and [Maven ≥ 3.5.4](https://maven.apache.org/download.cgi))
* .NET ([.NET Core ≥ 3.1](https://dotnet.microsoft.com/download))
* Go ([Go ≥ 1.16.4](https://golang.org/))
  - Go está atualmente em visualização do desenvolvedor e não é recomendado para uso em produção.

\
Pule para:
[Developer Guide](https://docs.aws.amazon.com/cdk/latest/guide) |
[API Reference](https://docs.aws.amazon.com/cdk/api/latest/docs/aws-construct-library.html) |
[Getting Started](#getting-started) |
[Getting Help](#getting-help) |
[Contributing](#contributing) |
[RFCs](https://github.com/aws/aws-cdk-rfcs) |
[Roadmap](https://github.com/aws/aws-cdk/blob/master/ROADMAP.md) |
[More Resources](#more-resources)

-------

Os desenvolvedores usam a [estrutura CDK] em uma das linguagens de programação suportadas 
para definir componentes de nuvem reutilizáveis chamados [construções], que são compostos 
juntos em [pilhas], formando um "aplicativo CDK".

Em seguida, eles usam a [AWS CDK CLI] para interagir com o aplicativo CDK. A CLI permite 
que os desenvolvedores sintetizem artefatos como Modelos do AWS CloudFormation, implantem 
pilhas para contas de desenvolvimento da AWS e "diferenciem" uma pilha implantada para entender 
o impacto de uma alteração de código.

A [AWS Construct Library] inclui um módulo para cada serviço da AWS com construções que 
oferecem APIs avançadas que encapsulam os detalhes de como usar a AWS. A AWS Construct Library visa 
reduzir a complexidade e a lógica necessária ao integrar vários serviços da AWS para atingir seus objetivos na AWS.

Os módulos na AWS Construct Library são designados Experimental enquanto os construímos; 
os módulos experimentais podem ter alterações de API importantes em qualquer versão.  Depois 
que um módulo é designado como Estável, ele adere ao [controle de versão semântico](https://semver.org/) 
e apenas as versões principais podem ter alterações importantes.
A designação de estabilidade de cada módulo está disponível em sua 
página Visão geral no [AWS CDK API Reference](https://docs.aws.amazon.com/cdk/api/latest/docs/aws-construct-library.html).
Para obter mais informações, consulte [Versionamento](https://docs.aws.amazon.com/cdk/latest/guide/reference.html#versioning)
no Guia do desenvolvedor do CDK.

[CDK framework]: https://docs.aws.amazon.com/cdk/latest/guide/home.html
[constructs]: https://docs.aws.amazon.com/cdk/latest/guide/constructs.html
[stacks]: https://docs.aws.amazon.com/cdk/latest/guide/stacks.html
[apps]: https://docs.aws.amazon.com/cdk/latest/guide/apps.html
[Developer Guide]: https://docs.aws.amazon.com/cdk/latest/guide
[AWS CDK CLI]: https://docs.aws.amazon.com/cdk/latest/guide/tools.html
[AWS Construct Library]: https://docs.aws.amazon.com/cdk/api/latest/docs/aws-construct-library.html


## Começando

Para um passo a passo detalhado, consulte o [tutorial](https://docs.aws.amazon.com/cdk/latest/guide/getting_started.html#hello_world_tutorial) in the AWS CDK [Developer Guide](https://docs.aws.amazon.com/cdk/latest/guide/home.html).

### Num relance
Instale ou atualize o [AWS CDK CLI] do npm (requer [Node.js ≥ 10.13.0](https://nodejs.org/download/release/latest-v10.x/)). Recomendamos o uso de uma versão em [Active LTS](https://nodejs.org/en/about/releases/)
⚠️ as versões `13.0.0` a `13.6.0` não são suportadas devido a problemas de compatibilidade com nossas dependências.

```console
$ npm i -g aws-cdk
```

(See [Manual Installation](./MANUAL_INSTALLATION.md) for installing the CDK from a signed .zip file).

Initialize a project:

```console
$ mkdir hello-cdk
$ cd hello-cdk
$ cdk init sample-app --language=typescript
```

Isso cria um projeto de amostra parecido com este:

```ts
export class HelloCdkStack extends cdk.Stack {
  constructor(scope: cdk.App, id: string, props?: cdk.StackProps) {
    super(scope, id, props);

    const queue = new sqs.Queue(this, 'HelloCdkQueue', {
      visibilityTimeout: cdk.Duration.seconds(300)
    });

    const topic = new sns.Topic(this, 'HelloCdkTopic');

    topic.addSubscription(new subs.SqsSubscription(queue));
  }
}
```

Implante isso em sua conta:

```console
$ cdk deploy
```

Use o kit de ferramentas de linha de comando `cdk` para interagir com seu projeto:

 * `cdk deploy`: deploys your app into an AWS account
 * `cdk synth`: synthesizes an AWS CloudFormation template for your app
 * `cdk diff`: compares your app with the deployed stack

## Conseguindo ajuda

A melhor forma de interagir com nossa equipe é através do GitHub. Você pode abrir um [problema](https://github.com/aws/aws-cdk/issues/new/choose) e escolher um de nossos modelos para relatórios de bugs, solicitações de recursos, problemas de documentação ou orientação.

Se você tiver um plano de suporte com o AWS Support, também poderá criar um novo [caso de suporte](https://console.aws.amazon.com/support/home#/).

Você também pode encontrar ajuda nestes recursos da comunidade:
*Consulte a [Referência da API](https://docs.aws.amazon.com/cdk/api/latest/docs/aws-construct-library.html) ou o [Guia do desenvolvedor](https://docs.aws. amazon.com/cdk/latest/guide)
* The #aws-cdk Slack channel in [cdk.dev](https://cdk.dev)
* Ask a question on [Stack Overflow](https://stackoverflow.com/questions/tagged/aws-cdk)
  and tag it with `aws-cdk`

## Roadmap

The [AWS CDK Roadmap project board](https://github.com/orgs/aws/projects/7) lets developers know about our upcoming features and priorities to help them plan how to best leverage the CDK and identify opportunities to contribute to the project. See [ROADMAP.md](https://github.com/aws/aws-cdk/blob/master/ROADMAP.md) for more information and FAQs.

## Contributing

We welcome community contributions and pull requests. See
[CONTRIBUTING.md](./CONTRIBUTING.md) for information on how to set up a development
environment and submit code.

## Metrics collection
This solution collects anonymous operational metrics to help AWS improve the
quality and features of the CDK. For more information, including how to disable
this capability, please see the 
[developer guide](https://docs.aws.amazon.com/cdk/latest/guide/cli.html#version_reporting).

## More Resources
* [CDK Workshop](https://cdkworkshop.com/)
* **[CDK Construction Zone](https://www.twitch.tv/collections/9kCOGphNZBYVdA)** - A Twitch live coding series hosted by the CDK team, season one episodes:
  * Triggers: Join us as we implement [Triggers](https://github.com/aws/aws-cdk-rfcs/issues/71), a Construct for configuring deploy time actions. Episodes 1-3:
    * [S1E1](https://www.twitch.tv/videos/917691798): Triggers (part 1); **Participants:** @NetaNir, @eladb, @richardhboyd
    * [S1E2](https://www.twitch.tv/videos/925801382): Triggers (part 2); **Participants:** @NetaNir, @eladb, @iliapolo 
    * [S1E3](https://www.twitch.tv/videos/944565768): Triggers (part 3); **Participants:** @NetaNir, @eladb, @iliapolo, @RomainMuller
  * [S1E4](https://www.twitch.tv/aws/video/960287598): [Tokens](https://docs.aws.amazon.com/cdk/latest/guide/tokens.html) Deep Dive; **Participants:** @NetaNir,@rix0rrr, @iliapolo, @RomainMuller
  * [S1E5](https://www.twitch.tv/videos/981481112): [Assets](https://docs.aws.amazon.com/cdk/latest/guide/assets.html) Deep Dive; **Participants:** @NetaNir, @eladb, @jogold
  * [S1E6](https://www.twitch.tv/aws/video/1005334364): [Best Practices](https://aws.amazon.com/blogs/devops/best-practices-for-developing-cloud-applications-with-aws-cdk/); **Participants:** @skinny85, @eladb, @rix0rrr, @alexpulver
  * [S1E7](https://www.twitch.tv/videos/1019059654): Tips and Tricks From The CDK Team; **Participants:** All the CDK team! 
* [Examples](https://github.com/aws-samples/aws-cdk-examples)
* [Changelog](./CHANGELOG.md)
* [NOTICE](./NOTICE)
* [License](./LICENSE)
