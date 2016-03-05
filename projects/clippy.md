---
layout: project
project: clippy
permalink: /projects/clippy-service/

features:
  - name: Higher Code Quality
    desc: Linting and Stylechecker are important tools to keep the code quality up. Having them automatically run and confirm your work ensures and encourages better code maintainance.
    icon_url: /assets/icons/code.svg

  - name: Free Status Badge
    desc: "From its very first version, the clippy-service rendered the status in great status badges, you can be proud to share on your readme: [![Clippy Linting Result](http://clippy.bashy.io/github/ligthyear/clippy-service/master/badge.svg)](http://clippy.bashy.io/github/ligthyear/clippy-service/master/log)"
    icon_url: /assets/icons/tag.svg

  - name: Fully Annotated Source Code
    desc: Further more, this project is part of an ongoing effort of [Are We Web yet](/projects/arewewebyet/) to improve the Rust Web Ecosystem. Clippy is an Example Project with [complete source code annotation](http://clippy.bashy.io/docs/) for others to learn how to build their project.
    icon_url: /assets/icons/book.svg
---

The [Clippy Service](http://clippy.bashy.io) is a Rust Project Linting service based on the great clippy-rust code style checker.

{% include components/features.html features=page.features %}
