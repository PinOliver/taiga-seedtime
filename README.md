# Taiga Seedtime

Taiga Seedtime is an agile estimation solution linked to Taiga. Taiga users can load their projects and estimate the relative weight of user stories chosen in a very fast way with this tool.

## Installation

### Taiga Front Plugin

This plugin affects the gulp compilation process so you need a working [taiga-front](https://github.com/taigaio/taiga-front) development environment to use it.

Copy in your `taiga-front/app/modules/compile-modules` directory of [Taiga front](https://github.com/taigaio/taiga-front) the `taiga-seedtime/contrib-front/taiga-contrib-seedtime` code.

Now when executing "gulp" or "gulp deploy" this plugin will be compiled and included too.

Include in your dist/conf.json the seedTimeUrl:

```json
  "seedTimeUrl": "http://localhost:8080"
```

### Taiga Back Plugin

Activate your Taiga virtualenv and install this package:

```bash
pip install "git+https://github.com/taigaio/taiga-seedtime.git@stable#egg=taiga_seedtime&subdirectory=back"
```

Modify your `settings/config.py` and include the line:

```python
  INSTALLED_APPS += ["taiga_seedtime"]
```

### Run Seedtime

```bash
cd taiga-seedtime/seedtime

npm install

cp static/env.js.sample static/env.js

## Edit static/env.js

npm start

## Taiga Seedtime is available at http://localhost:8080
```

**Admin Games Panel**

http://localhost:8000/admin/

    admin / 123123

**API Endpoint**

http://localhost:8000/api/v1/games/

## Documentation

Currently, we have authored three main documentation hubs:

- **[API](https://docs.taiga.io/api.html)**: Our API documentation and reference for developing from Taiga API.
- **[Documentation](https://docs.taiga.io/)**: If you need to install Taiga on your own server, this is the place to find some guides.
- **[Taiga Community](https://community.taiga.io/)**: This page is intended to be the support reference page for the users.

## Bug reports

If you **find a bug** in Taiga you can always report it:

- in [Taiga issues](https://tree.taiga.io/project/taiga/issues). **This is the preferred way**
- in [Github issues](https://github.com/taigaio/taiga-seedtime/issues)
- send us a mail to support@taiga.io if is a bug related to [tree.taiga.io](https://tree.taiga.io)
- send us a mail to security@taiga.io if is a **security bug**

One of our fellow Taiga developers will search, find and hunt it as soon as possible.

Please, before reporting a bug, write down how can we reproduce it, your operating system, your browser and version, and if it's possible, a screenshot. Sometimes it takes less time to fix a bug if the developer knows how to find it.

## Community

If you **need help to setup Taiga**, want to **talk about some cool enhancemnt** or you have **some questions**, please go to [Taiga community](https://community.taiga.io/).

If you want to be up to date about announcements of releases, important changes and so on, you can subscribe to our newsletter (you will find it by scrolling down at [https://taiga.io](https://www.taiga.io/)) and follow [@taigaio](https://twitter.com/taigaio) on Twitter.

## Contribute to Taiga

There are many different ways to contribute to Taiga's platform, from patches, to documentation and UI enhancements, just find the one that best fits with your skills. Check out our detailed [contribution guide](https://community.taiga.io/t/how-can-i-contribute/159#code-patches-enhacements-3).

## Code of Conduct

Help us keep the Taiga Community open and inclusive. Please read and follow our [Code of Conduct](https://github.com/taigaio/code-of-conduct/blob/main/CODE_OF_CONDUCT.md).

## License

Every code patch accepted in Taiga codebase is licensed under [MPL 2.0](LICENSE). You must be careful to not include any code that can not be licensed under this license.

Please read carefully [our license](LICENSE) and ask us if you have any questions as well as the [Contribution policy](https://github.com/taigaio/taiga-seedtime/blob/main/CONTRIBUTING.md).
