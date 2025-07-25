# Military System Simulation

A Java Swing-based military command and control system simulation that demonstrates the **Observer Design Pattern**. This application simulates a military operation control center where a main controller can communicate with and coordinate multiple military units including helicopters, tanks, and submarines.

## 🎯 Features

### Core Functionality
- **Multi-Unit Command System**: Control helicopters, tanks, and submarines from a central command interface
- **Real-time Communication**: Send messages and commands between units and main controller
- **Position Control**: Adjust unit positions using slider controls
- **Area Status Management**: Monitor and control area clearance status
- **Weapon Systems**: Each unit has specific weapon capabilities
- **Resource Tracking**: Monitor soldier count, ammunition, fuel, and other unit-specific resources

### Military Units

#### 🚁 Helicopter
- **Weapons**: Laser operation, Missile operation, Shooting capabilities
- **Resources**: Soldier count, Ammunition count
- **Special Features**: Air-based positioning, Message communication system

#### 🛡️ Tank
- **Weapons**: Missile operation, Radar operation, Rotate operation, Shooting capabilities
- **Resources**: Soldier count, Ammunition count
- **Special Features**: Ground-based positioning, Advanced radar systems

#### 🌊 Submarine
- **Weapons**: Sonar operation, Tomahawk missiles, Trident-2 missiles, Shooting capabilities
- **Resources**: Soldier count, Ammunition count, Energy levels, Oxygen levels
- **Special Features**: Underwater positioning, Dual resource management (Energy & Oxygen)

## 🏗️ Architecture

### Design Patterns
- **Observer Pattern**: The system implements a robust observer pattern where:
  - `Observer` class acts as the central coordinator
  - `Observable` interface defines the contract for military units
  - All military units implement the `Observable` interface
  - Main controller can broadcast commands to all units or specific unit types

### Class Structure
```
militarysystem/
├── Starter.java          # Application entry point
├── Observer.java         # Central command coordinator (Observer)
├── Observable.java       # Interface for military units
├── MainController.java   # Main command center GUI
├── Helicopter.java       # Helicopter unit implementation
├── Tank.java            # Tank unit implementation
├── Submarine.java       # Submarine unit implementation
└── *.form               # NetBeans form files for GUI design
```

## 🚀 Getting Started

### Prerequisites
- **Java 11** or higher
- **NetBeans IDE** (recommended for development)
- **Apache Ant** (for building via command line)

### Running the Application

#### Using NetBeans IDE
1. Open the project in NetBeans IDE
2. Right-click on the project and select "Run"
3. The application will start and display all military unit windows

#### Using Command Line
```bash
# Navigate to project directory
cd /path/to/MilitarySystem

# Build the project
ant build

# Run the application
java -cp build/classes militarysystem.Starter
```

## 🎮 How to Use

1. **Start Application**: Run the `Starter` class to launch all military unit windows
2. **Main Controller**: Use the main controller window to:
   - Select target units (All, Helicopter, Tank, or Submarine)
   - Send messages to units
   - Control area clearance status
   - Adjust unit positions using the slider
   - Toggle private/public communication mode

3. **Unit Operations**: Each unit window allows you to:
   - Monitor current status and resources
   - Execute unit-specific weapon operations
   - Send messages back to command
   - Adjust position settings
   - View incoming messages from command

4. **Communication Flow**:
   - Commands flow from Main Controller → Observer → Military Units
   - Status updates flow from Military Units → Observer → Main Controller

## 🛠️ Technical Details

### Development Environment
- **IDE**: NetBeans (with form designer)
- **Build System**: Apache Ant
- **GUI Framework**: Java Swing
- **Java Version**: 11
- **Project Type**: NetBeans Java Application

### Key Components
- **Observer Pattern Implementation**: Centralized command distribution
- **Swing GUI**: Multi-window interface with form-based design
- **Resource Management**: Real-time tracking of unit capabilities
- **Message Broadcasting**: Flexible communication system

## 📁 Project Structure

```
MilitarySystem/
├── build.xml                    # Ant build configuration
├── manifest.mf                  # JAR manifest file
├── build/                       # Compiled classes directory
│   └── classes/militarysystem/  # Compiled .class files
├── nbproject/                   # NetBeans project configuration
│   ├── build-impl.xml
│   ├── project.properties
│   └── project.xml
├── src/militarysystem/          # Source code
│   ├── *.java                   # Java source files
│   └── *.form                   # NetBeans form files
└── test/                        # Test directory (empty)
```

## 🔧 Build Configuration

The project uses standard NetBeans/Ant build configuration:
- **Source/Target**: Java 17
- **Main Class**: `militarysystem.Starter`
- **JAR Name**: `MilitarySystem.jar`
- **Compile on Save**: Enabled in NetBeans


## 📝 License

This project is open source and available for educational purposes. Feel free to use, modify, and distribute as needed.

## 👤 Author

⭐️ From [Nugi29](https://github.com/Nugi29)

---

*This simulation is designed for educational purposes to demonstrate software design patterns and GUI programming concepts in Java.*
