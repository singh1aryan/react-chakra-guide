## Introduction

Chakra UI is a React component library that helps you build accessible, composable, and customizable user interfaces. It is built on top of the popular design system, Chakra, and uses Emotion for styling.

To use Chakra UI in a React project, you need to first install it from npm:

```bash
npm install @chakra-ui/core
```

Once installed, you can import and use the Chakra UI components in your React components:

```jsx
import { Button } from "@chakra-ui/core"

function MyButton() {
  return <Button>Click me!</Button>
}
```

Chakra UI provides a wide range of pre-built components that you can use to build your user interface, such as buttons, form inputs, layout containers, and more. It also provides various utility functions and hooks to help you manage styles, colors, and other aspects of your UI.

Chakra UI follows the principles of accessibility, composability, and customization. This means that all of its components are built with accessibility in mind, they can be easily composed and nested to build complex UIs, and they can be customized using props and theme values to match your app's design.

Overall, Chakra UI is a powerful and flexible tool for building user interfaces with React. It is well-documented and actively maintained, making it a great choice for developers who want to quickly and easily build accessible and customizable UIs.

## Simple form website

Here is a bigger example that shows how to use some of the core components from Chakra UI to build a simple login form:

```jsx
import React from "react"
import {
  Box,
  FormControl,
  FormLabel,
  Input,
  Button,
  Flex,
  Text,
} from "@chakra-ui/core"

function LoginForm() {
  return (
    <Box p={4} w="300px">
      <FormControl>
        <FormLabel htmlFor="email">Email</FormLabel>
        <Input type="email" id="email" placeholder="Enter your email" />
      </FormControl>
      <FormControl mt={4}>
        <FormLabel htmlFor="password">Password</FormLabel>
        <Input type="password" id="password" placeholder="Enter your password" />
      </FormControl>
      <Flex mt={4} justifyContent="space-between">
        <Button variantColor="teal" type="submit">
          Login
        </Button>
        <Text fontSize="sm">Forgot password?</Text>
      </Flex>
    </Box>
  )
}
```

In this example, we have used the **`Box`** component from Chakra UI to create a container for the form. Inside the container, we have used the **`FormControl`**, **`FormLabel`**, and **`Input`** components to create a form with two input fields for the email and password.

We have also used the **`Button`** and **`Flex`** components to create a login button and a "Forgot password?" link at the bottom of the form. Finally, we have used the **`Text`** component to style the link text.

Overall, this example shows how Chakra UI's components can be easily combined to create a simple, but functional login form.

## Simple portfolio website

Here is an example of how you can use Chakra UI and React to create a simple portfolio website:

```jsx
import React from "react"
import {
  Box,
  Flex,
  Text,
  Image,
  Heading,
  Link,
  Stack,
  Divider,
} from "@chakra-ui/core"

function Portfolio() {
  return (
    <Box>
      <Flex alignItems="center" justifyContent="center" mt={4}>
        <Image
          src="https://via.placeholder.com/150"
          alt="Your profile image"
          rounded="full"
        />
      </Flex>
      <Heading mt={4} textAlign="center" fontSize="2xl">
        Your Name
      </Heading>
      <Text mt={2} textAlign="center" fontSize="lg">
        Job Title
      </Text>
      <Text mt={2} textAlign="center" fontSize="md">
        Company Name
      </Text>
      <Divider my={8} />
      <Heading as="h2" mt={4} fontSize="xl">
        About Me
      </Heading>
      <Text mt={2} fontSize="md">
        Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod
        tempor incididunt ut labore et dolore magna aliqua.
      </Text>
      <Divider my={8} />
      <Heading as="h2" mt={4} fontSize="xl">
        Projects
      </Heading>
      <Stack mt={4} spacing={4}>
        <Flex alignItems="center">
          <Image src="https://via.placeholder.com/150" alt="Project image" />
          <Link ml={4} fontSize="md" href="#">
            Project 1
          </Link>
        </Flex>
        <Flex alignItems="center">
          <Image src="https://via.placeholder.com/150" alt="Project image" />
          <Link ml={4} fontSize="md" href="#">
            Project 2
          </Link>
        </Flex>
        <Flex alignItems="center">
          <Image src="https://via.placeholder.com/150" alt="Project image" />
          <Link ml={4} fontSize="md" href="#">
            Project 3
          </Link>
        </Flex>
      </Stack>
    </Box>
  )
}
```

In this example, we have used the **`Box`**, **`Flex`**, **`Text`**, **`Image`**, **`Heading`**, **`Link`**, **`Stack`**, and **`Divider`** components from Chakra UI to create a simple portfolio website.

The website has a header with the user's profile image, name, job title, and company name. It also has an "About Me" section where the user can write a brief description of themselves, and a "Projects" section where they can list their projects with images and links.

Overall, this example shows how Chakra UI's components can be used to create a clean and simple portfolio website with React.

## Simple Gallery app

1. Install the necessary dependencies, including React, Chakra UI, and any other libraries you might need.
2. Create a new React project using **`create-react-app`** or another tool of your choice.
3. Set up the Chakra UI theme and provider in your **`App.js`** file, so that the Chakra components can be used throughout your application.
4. Create a new component to display the photo gallery, and import the necessary Chakra UI components, such as **`Box`**, **`Image`**, and **`Stack`**.
5. Use the Chakra UI components to create a grid layout for the photos, and load the photos from an array of image URLs or from a remote API.
6. Add functionality to allow the user to view a full-size version of the photos by clicking on them, or by using a modal or lightbox component.
7. Add other features, such as filtering or sorting options, to allow the user to customize the photo gallery.
8. Test the app to make sure it works as expected, and make any necessary adjustments.
9. Deploy the app to a hosting service, such as Heroku or Netlify, so that others can access it.

Overall, creating a photo gallery app with Chakra UI and React will require some knowledge of React, Chakra UI, and CSS, as well as a basic understanding of web development concepts and tools. However, with the right resources and guidance, it can be a fun and rewarding project that showcases your skills and creativity.

Here is an example of how you could create a simple photo gallery app with Chakra UI and React:

```jsx
import React from 'react';
import { Box, Image, Stack } from '@chakra-ui/core';

// Create the PhotoGallery component
const PhotoGallery = () => {
  // Define an array of image URLs
  const images = [
    'https://picsum.photos/id/1/300/300',
    'https://picsum.photos/id/2/300/300',
    'https://picsum.photos/id/3/300/300',
    'https://picsum.photos/id/4/300/300',
    'https://picsum.photos/id/5/300/300',
  ];

  // Use the Chakra UI Stack component to create a grid layout for the photos
  return (
    <Stack spacing={4}>
      {images.map((image, index) => (
        <Box key={index}>
          <Image src={image} />
        </Box>
      ))}
    </Stack>
  );
};

export default PhotoGallery;
```

In this example, the **`PhotoGallery`** component creates a grid layout for the photos using the **`Stack`** component from Chakra UI. The photos are loaded from an array of image URLs, and each photo is displayed using the **`Box`** and **`Image`** components from Chakra UI. You can customize the layout and functionality of the photo gallery by using different Chakra UI components and adding additional features, such as filtering or sorting options.

## Simple TODO list

Here is an example of how you could create a simple todo website with Chakra UI and React:

```jsx
import React, { useState } from 'react';
import {
  Box,
  Button,
  Flex,
  FormControl,
  FormLabel,
  Input,
  Stack,
  Text,
} from '@chakra-ui/core';

// Create the TodoList component
const TodoList = () => {
  // Use React's useState hook to manage the list of todos
  const [todos, setTodos] = useState([]);

  // Define a function to add a new todo to the list
  const addTodo = (todo) => {
    setTodos([...todos, todo]);
  };

  // Define a function to remove a todo from the list
  const removeTodo = (index) => {
    setTodos(todos.filter((_, i) => i !== index));
  };

  return (
    <Box>
      {/* Use the Chakra UI Flex component to create a form for adding new todos */}
      <Flex mt={4} align="center">
        <FormControl>
          <FormLabel htmlFor="new-todo">New Todo</FormLabel>
          <Input
            id="new-todo"
            placeholder="Enter a new todo"
            onKeyPress={(event) => {
              if (event.key === 'Enter') {
                addTodo(event.target.value);
                event.target.value = '';
              }
            }}
          />
        </FormControl>
      </Flex>

      {/* Use the Chakra UI Stack component to create a list of todos */}
      <Stack mt={4} spacing={4}>
        {todos.map((todo, index) => (
          <Box key={index}>
            <Text>{todo}</Text>
            <Button onClick={() => removeTodo(index)}>Remove</Button>
          </Box>
        ))}
      </Stack>
    </Box>
  );
};

export default TodoList;
```

In this example, the **`TodoList`** component uses the **`useState`** hook to manage the list of todos. The component includes a form for adding new todos, which adds the new todo to the list when the user presses the **`Enter`** key. The component also includes a list of todos, which displays each todo in the list and includes a button for removing the todo. You can customize the layout and functionality of the todo list by using different Chakra UI components and adding additional features, such as sorting or filtering options.

## Simple traveling app

```jsx
import { Input, InputGroup, InputLeftAddon } from '@chakra-ui/react';
import { Center, Square, Circle } from '@chakra-ui/react'
import { Flex, Spacer } from '@chakra-ui/react'
import { Text } from '@chakra-ui/react'
import { Select } from '@chakra-ui/react'
import { Button, ButtonGroup, Stack } from '@chakra-ui/react'
import { useState, useEffect } from "react"
import { FormControl, FormLabel } from "@chakra-ui/react"

import { AirbnbCard } from './card'

function HomePage() {
    const [places, setPlaces] = useState([]);
    const [selectedState, setSelectedState] = useState('');
    const [numDays, setNumDays] = useState(0);

    const handleSubmit = () => {
        // Fetch places based on selected state and number of days
        try {
            fetch(`https://some-place-api.com/places?state=${selectedState}&days=${numDays}`)
                .then(response => response.json())
                .then(data => setPlaces(data));
        } catch (error) {
            console.log(error)
        }
    }

    return (<div>
        <Stack>
            {/* Input for selecting state */}
            <input
                type="text"
                placeholder="Enter a state"
                value={selectedState}
                onChange={e => setSelectedState(e.target.value)}
            />

            {/* Input for selecting number of days */}
            <input
                type="number"
                placeholder="Enter number of days"
                value={numDays}
                onChange={e => setNumDays(e.target.value)}
            />

            {/* Button to submit form and fetch places */}
            <Button onClick={handleSubmit}>
                Submit
            </Button>

            {/* List of places */}
            <ul>
                {places.map(place => (
                    <li key={place.id}>{place.name}</li>
                ))}
            </ul>
        </Stack>

    </div>)
}

export default HomePage
```
