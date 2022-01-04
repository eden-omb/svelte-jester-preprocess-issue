# Reproducing this repo
Go in a new folder and do the following:
* Run `pnpm init svelte@next .`
* Run `pnpx apply rossyman/svelte-add-jest --no-ssh`
* Run `pnpm install`
* Run `pnpm test` and observe the tests working
* Add the `preprocessing` option to `svelte-jester` in `jest.config.json`
* Run `pnpm test` and observe tests failing with the following:

```
 FAIL  src/routes/index-dom.spec.js
  ● Test suite failed to run

    TypeError: The "id" argument must be of type string. Received an instance of URL

      at node_modules/.pnpm/svelte-jester@2.1.5_jest@27.4.5+svelte@3.44.3/node_modules/svelte-jester/dist/transformer.cjs:79:118

Test Suites: 1 failed, 1 total
Tests:       0 total
Snapshots:   0 total
Time:        1.534 s, estimated 2 s
Ran all test suites matching /src/i.
 ERROR  Test failed. See above for more details.
```
