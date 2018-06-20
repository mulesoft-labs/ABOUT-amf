<p align="center">
  <img alt="ABOUT-cli Logo" src="https://user-images.githubusercontent.com/1119553/34323079-3fc331c0-e7ee-11e7-8882-c14750a52f74.png" height="80" />
  <h3 align="center">ABOUT-amf</h3>
  <p align="center">AML/AMF vocabularies, dialects and validations for ABOUT.</p>
  <p align="center">
    <a href="/LICENSE"><img alt="Software License" src="https://img.shields.io/badge/license-Apache%202-blue.svg?style=flat-square"></a>
    <a href="https://saythanks.io/to/vromero"><img alt="SayThanks.io" src="https://img.shields.io/badge/SayThanks.io-%E2%98%BC-1EAEDB.svg?style=flat-square"></a>
  </p>
</p>

---

The `ABOUT-amf` repository contains (and exposes through HTTP) [AML/AMF](http://a.ml) vocabularies, dialects and valudations. Such artifacts enable the parsing, validation and transformation of ABOUT files.

These files attempt to describe with fidelity the human friendly specification avaiable in the [*ABOUT*](https://github.com/mulesoft-labs/ABOUT) repository.

[*ABOUT*](https://github.com/mulesoft-labs/ABOUT) is a software project metadata file format.

## Community, discussion, contribution, and support

You can reach to the *ABOUT* server developers via the following channels:

- GitHub [issue tracker](https://github.com/mulesoft-labs/ABOUT-amf/issues)

### Code of conduct

This project adheres to the Contributor Covenant code of conduct. By participating, you are expected to 
uphold this code. We appreciate your contribution. Please refer to our [contributing guidelines](CODE_OF_CONDUCT.md) for further information.

## Related Projects

*ABOUT* is both a specification and the tooling that implements it. The following is a list with the repositories of
those projects:

- [**ABOUT** specificaton](https://github.com/mulesoft-labs/ABOUT).
- [**ABOUT** command line tool](https://github.com/mulesoft-labs/ABOUT-cli).
A command line tool to infer, transform and validate ABOUT files.
- [**ABOUT** GitHub App](https://github.com/mulesoft-labs/ABOUT-github-app). A GitHub application, that validates pull requests, fetch ABOUT files and send to the `ABOUT-server`.
- [**ABOUT** Server](https://github.com/mulesoft-labs/ABOUT-server). A server that receives and validates ABOUT files, to store them 
in a triple store. It does also provide a SPARQL endpoint to query the files.
- [**ABOUT** Query GUI](https://github.com/mulesoft-labs/ABOUT-query-gui). A query GUI that connects to the ABOUT server.
- [**ABOUT**-dashboard](https://github.com/mulesoft-labs/ABOUT-dashboard) an [inner source](https://en.wikipedia.org/wiki/Inner_source) dashboard for organizations using ABOUT.
- [**ABOUT**-amf](https://github.com/mulesoft-labs/ABOUT-amf) repository provides an [AMF](https://a.ml) dialect and vocabulary. With AMF and these files, its possible to parse, transform and validate ABOUT files in any JVM language and JavaScript. The `about-cli` and `about-server` are examples of applications using AMF to work with ABOUT files.
- [**ABOUT**-helm-chart](https://github.com/mulesoft-labs/ABOUT-helm-chart) a [Helm](https://helm.sh) chart to ease the installation of the server side tooling into Kubernetes.

```
+-----------+     +------------+    +--------+   +------------------+
| ABOUT cli +-----> ABOUT.yaml +----> GitHub +---> ABOUT github app |
+-----^-----+     +--^---------+    +--------+   +------+-----------+
      |              |                |                 |
      |              |                |                 |
      +              |    +-----------v-----+    +------v-------+     +------------------+
  ((USER))+----------+----> ABOUT query gui |    | ABOUT server <-----+ ABOUT dashboard  |
                          +-----------------+    +--------------+     +------------------+
                                                   |
                                                   |
                                            +------v-------+
                                            | Triple store |
                                            +--------------+
```