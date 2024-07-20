# Micro Frontend Application with Pokémon API

## Overview
This project demonstrates a micro frontend architecture consisting of a host application and multiple remote applications. The host application manages the communication between the remote applications, allowing dynamic content updates based on user interaction. The remote applications consume the Pokémon API to display Pokémon images and names.

## Host Application
The host application serves as the main shell that mounts the remote applications. It is responsible for setting up the necessary configurations and maintaining active communication with the remote applications.

### Features
**Basic Configurations**:
- Set up as a micro frontend host/shell.
- Mounts and displays remote applications.

**Active Communication**:
- Uses Custom Events, EventEmitter, or RXJS for communication.
- Sends messages to remote applications to trigger content changes via a "Change" button.

### Implementation Details
**Communication**:
- Utilizes Custom Events to send messages from the host to the remote applications.
- On clicking the "Change" button, the host emits an event that the remote applications listen to and respond by updating their content.

## Remote Applications
Each remote application is responsible for consuming the Pokémon API and rendering the Pokémon's image and name. The remote applications respond to messages from the host application to update the displayed Pokémon.

### Features
**API Consumption**:
- Consumes the Pokémon API at `https://pokeapi.co/api/v2/pokemon/{id or name}`.
- Examples:
  - `https://pokeapi.co/api/v2/pokemon/pikachu`
  - `https://pokeapi.co/api/v2/pokemon/charmander`
  - `https://pokeapi.co/api/v2/pokemon/bulbasaur`

**Content Rendering**:
- Displays the Pokémon's image and name at the center of the component.
- Updates the displayed Pokémon upon receiving a message from the host application.

## Usability and Reusability
The project follows best practices for usability and reusability of components, ensuring modularity, optimization, and adherence to design patterns.

Presentado por: Jefferson Almanza
