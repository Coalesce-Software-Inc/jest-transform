# jest-transform

This package fixes an issue in the mainline jest transform for our environment.

It was built from https://github.com/Coalesce-Software-Inc/jest, commit [492c46d2bc45ee9d4de5aededeaa95e763aa92e5](https://github.com/Coalesce-Software-Inc/jest/commit/492c46d2bc45ee9d4de5aededeaa95e763aa92e5), the tip of the [coalesce](https://github.com/Coalesce-Software-Inc/jest/commits/coalesce) branch. That commit is based on `v29.7.0` of Jest.

Build Procedure:

```bash
git clone --branch coalesce https://github.com/Coalesce-Software-Inc/jest.git
cd jest
nvm use v21.2.0
yarn install
yarn build

```

Then the contents of `jest/packages/jest-transform` was copied to this repository.

Finally, the `package.json` from the repo was overwritten using the "official" one [here](https://www.npmjs.com/package/@jest/transform?activeTab=code).

```bash
curl https://www.npmjs.com/package/@jest/transform/file/7b780a1a5a7c2b21ec7bd829301213835db61a2b60a01535d5b4a8380aeeebf5 > package.json
```
