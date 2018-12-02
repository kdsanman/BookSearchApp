# Book Search App

## App Description
Android app that leverages the [OpenLibrary API](https://openlibrary.org/developers/api) to search books and display cover images. This app is to be used as the base app for adding suggested extensions.

## Overview

The app does the following:

1. Fetches the books from the [OpenLibrary Search API](https://openlibrary.org/dev/docs/api/search) in JSON format
2. Deserializes the JSON data for each of the books into `Book` objects
3. Builds an array of `Book` objects and notifies the adapter to display the new data
4. Defines a view holder so the adapter can render each book model
5. Uses SearchView to search for books with a title


To achieve this, there are four different components in this app:

1. `BookClient` - Responsible for executing the API requests and retrieving the JSON
2. `Book` - Model object responsible for encapsulating the attributes for each individual book
3. `BookAdapter` - Responsible for mapping each `Book` to a particular view layout
4. `BookListActivity` - Responsible for fetching and deserializing the data and configuring the adapter

## Usage
This app is intended to be the base project on top of which new features can be added. It was cloned from [here](https://github.com/codepath/android-booksearch-exercise/).

## Libraries

This app leverages two third-party libraries:

 * [Android AsyncHTTPClient](http://loopj.com/android-async-http/) - For asynchronous network requests
