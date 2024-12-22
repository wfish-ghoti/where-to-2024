---
layout: page
---

# Before you start a tutorial: GET READY

These are the steps you must do before you can run
the tutorials for the **Where To service**.

Expect this preparation to take about 20 minutes to complete.

## Preparing for the tutorials

To complete the tutorials in this section, you need the following.
You might want to open the links in separate brower tabs before you start installing the software.

* A [GitHub account](https://github.com)
* A development system (PC, Mac, or Linux) running a current or
long-term support (LTS version of the operating system).
* The following software on your development system:
  * [Git](https://docs.github.com/en/get-started/quickstart/set-up-git) (for the command line)
  * [GitHub Desktop](https://desktop.github.com) (optional)
  * The [Postman desktop app](https://www.postman.com/downloads/). Because you run the **Where To service** on your development system with an `http://localhost` hostname, the web-version of Postman can't perform the exercises.
  * A current/LTS version of `node.js`
  * A current version of [json-server](https://www.npmjs.com/package/json-server)
* A fork of the [Where To repo](https://github.com/wfish-ghoti/where-to-2024.git)
* A current copy of the database file. You can get this by syncing your fork.

    **TIP**: If you're using a fork of the repo, create a working branch in which to do your tutorials. Create a new branch for each tutorial to prevent a mistake in one from affecting your work in another.

## Test your development system

To test your development system:.

1. Use GitHub Desktop or your preferred client to create and checkout a test branch of your fork of the Where To service repo. Your `GitHub repo workspace` is the directory that contains your fork of the `where-to-2024` repo.

    ```shell
    cd <your GitHub repo workspace>
    ls
    # (see the to-do-service directory in the list)
    cd where-to-2024
    git checkout -b tutorial-test
    cd api
    json-server -w to-do-db-source.json
    ```

    If your development system is installed correctly, you should see
    the service start and display the URL of the service: `http://localhost:3000`.

2. Make a test call to the service.

    ```shell
    curl http://localhost:3000/users
    ```

3. If the service is running correctly, you should see a list of users from the service, such as in this example.

    ```js
    [
        {
            "name": "Kathy Barnes",
            "location": "Los Angeles",
            "city_visited": "Split, Seattle, New York",
            "city_to_visit": "Tokyo, Sydney, Barcelona",
            "id": 1
        },
        {
            "name": "Rex Fieldman",
            "location": "Las Vegas",
            "city_visited": "Galway, London, Austin",
            "city_to_visit": "Delhi, Johannesburg, Paris",
            "id": 2
        },
        ...
    ```

If you don't see the list of users, or receive an error in any step
of the procedure, investigate and correct the error before continuing.
Some common situations that cause errors include:

1. You mistyped a command.
2. You aren't in the correct directory.
3. A required software component didn't install correctly.
4. A required software component isn't up to date.

If you see the list of users from the service, you're ready to do
the [quick start](WhereTo-LetsGo.md).

## Useful links

* [Check for updates](Updates.md).
* [Contact us](mailto:where-to@example.com).
