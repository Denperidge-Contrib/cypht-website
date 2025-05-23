---
title: Tests
exclude: true
---
<h2>Tests</h2>
<hr>
<p>
    Cypht uses PHPUnit to run our unit tests, and Selenium for integration testing. I periodically update the HTML
    coverage report located here:<br /><br /><a href="docs/test_coverage/index.html"
        title="Tests">/docs/test_coverage/index.html</a><br /><br />
    Currently our unit tests only cover the application framework (all the code under "lib/"), and the core
    module set, and our Selenium tests are still pretty basic. We make use of the following services that generously
    provide
    access to Open Source projects:<br />
</p>
<hr>
<h3>Travis CI</h3>
<a href="https://travis-ci.org/cypht-org/cypht/builds">https://travis-ci.org/cypht-org/cypht/builds</a>
<p>Travis CI is a really cool continuous integration service that we use to re-run our unit and UI tests every time
    a change is pushed to Github. Our Travis build is 18 combinations, 6 versions of PHP (5.4, 5.5, 5.6, 5.7, 7.0,
    7.1,
    7.2) with 3 different databases (Mysql, Postgresql, Sqlite). </p>
<hr>
<h3>BrowserStack</h3>
<a href="https://www.browserstack.com/">https://www.browserstack.com/</a><br /><br />
<p>BrowserStack is a cloud based Selenium grid we use to run our UI tests. We connect to it directly from Travis CI.
    Currently we test 4 browsers (Safari, IE, Edge, and Chrome). Firefox is disable for now due to a compatibility
    issue
    with the test environment.</p>
<hr>
<h3>Coveralls</h3>
<a href="https://coveralls.io/github/cypht-org/cypht">https://coveralls.io/github/cypht-org/cypht</a><br /><br />
<p>Coveralls.io provides access to the PHPUnit test coverage report, and is updated every time code is pushed to
    Github.
    It has some cool metrics to track unit test coverage over time, and in general is a nicer UI than the PHPUnit
    HTML
    report.</p>
<hr>
<h3>Scrutinizer</h3>
<a href="https://scrutinizer-ci.com/g/cypht-org/cypht/">https://scrutinizer-ci.com/g/cypht-org/cypht/</a><br /><br />
<p>Scrutinizer is a static code analyzer with a lot of great options. It understands our doc-string format and
    provides
    additinal information about potential type mismatches, in addition to a number of other static checks. Currently
    I have it limited to the application framework (all the code under "lib/"). Like the Travis builds and Coveralls
    reports,
    a new analysis is run every time we push code to Github.</p>