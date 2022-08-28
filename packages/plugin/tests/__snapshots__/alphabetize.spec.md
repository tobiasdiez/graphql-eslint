// Jest Snapshot v1, https://goo.gl/fbAQLP

exports[`Invalid #1 1`] = `
#### ⌨️ Code

      1 |         type User {
      2 |           password: String
      3 |           firstName: String!
      4 |           age: Int
      5 |           lastName: String!
      6 |         }

#### ⚙️ Options

    {
      "fields": [
        "ObjectTypeDefinition"
      ],
      "ignorePrefix": [],
      "ignoreSuffix": []
    }

#### ❌ Error 1/2

      2 |           password: String
    > 3 |           firstName: String!
        |           ^^^^^^^^^ \`firstName\` should be before \`password\`.
      4 |           age: Int

#### ❌ Error 2/2

      3 |           firstName: String!
    > 4 |           age: Int
        |           ^^^ \`age\` should be before \`firstName\`.
      5 |           lastName: String!

#### 🔧 Autofix output

      1 |         type User {
      2 |           age: Int
      3 |           firstName: String!
      4 |           lastName: String!
      5 |           password: String
      6 |         }
`;

exports[`Invalid #2 1`] = `
#### ⌨️ Code

      1 |         type User {
      2 |           password: String
      3 |           firstName: String!
      4 |           age: Int
      5 |           lastName: String!
      6 |         }

#### ⚙️ Options

    {
      "fields": [
        "ObjectTypeDefinition"
      ],
      "ignorePrefix": [
        "ID"
      ],
      "ignoreSuffix": []
    }

#### ❌ Error 1/2

      2 |           password: String
    > 3 |           firstName: String!
        |           ^^^^^^^^^ \`firstName\` should be before \`password\`.
      4 |           age: Int

#### ❌ Error 2/2

      3 |           firstName: String!
    > 4 |           age: Int
        |           ^^^ \`age\` should be before \`firstName\`.
      5 |           lastName: String!

#### 🔧 Autofix output

      1 |         type User {
      2 |           age: Int
      3 |           firstName: String!
      4 |           lastName: String!
      5 |           password: String
      6 |         }
`;

exports[`Invalid #3 1`] = `
#### ⌨️ Code

      1 |         extend type User {
      2 |           age: Int
      3 |           firstName: String!
      4 |           password: String
      5 |           lastName: String!
      6 |         }

#### ⚙️ Options

    {
      "fields": [
        "ObjectTypeDefinition"
      ],
      "ignorePrefix": [],
      "ignoreSuffix": [
        "ID"
      ]
    }

#### ❌ Error

      4 |           password: String
    > 5 |           lastName: String!
        |           ^^^^^^^^ \`lastName\` should be before \`password\`.
      6 |         }

#### 🔧 Autofix output

      1 |         extend type User {
      2 |           age: Int
      3 |           firstName: String!
      4 |           lastName: String!
      5 |           password: String
      6 |         }
`;

exports[`Invalid #4 1`] = `
#### ⌨️ Code

      1 |         interface Test {
      2 |           cc: Int
      3 |           bb: Int
      4 |           aa: Int
      5 |         }

#### ⚙️ Options

    {
      "fields": [
        "InterfaceTypeDefinition"
      ],
      "ignorePrefix": [],
      "ignoreSuffix": []
    }

#### ❌ Error 1/2

      2 |           cc: Int
    > 3 |           bb: Int
        |           ^^ \`bb\` should be before \`cc\`.
      4 |           aa: Int

#### ❌ Error 2/2

      3 |           bb: Int
    > 4 |           aa: Int
        |           ^^ \`aa\` should be before \`bb\`.
      5 |         }

#### 🔧 Autofix output

      1 |         interface Test {
      2 |           aa: Int
      3 |           bb: Int
      4 |           cc: Int
      5 |         }
`;
