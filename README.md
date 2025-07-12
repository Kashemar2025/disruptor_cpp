# Disruptor C++: A Lightweight LMAX Disruptor v3 Port in C++20 🚀

![GitHub Release](https://img.shields.io/github/release/Kashemar2025/disruptor_cpp.svg)
![License](https://img.shields.io/github/license/Kashemar2025/disruptor_cpp.svg)

## Table of Contents
- [Overview](#overview)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Examples](#examples)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

## Overview
The **Disruptor C++** library is a lightweight port of the LMAX Disruptor v3 for C++20. This implementation focuses on high throughput and low latency, making it ideal for applications that require efficient inter-thread communication. The Disruptor pattern is particularly useful in scenarios such as event processing, message queuing, and concurrent programming.

## Features
- **High Performance**: Achieves low latency and high throughput.
- **Thread-Safe**: Designed to handle multiple threads efficiently.
- **Simple API**: Easy to integrate into existing projects.
- **C++20 Support**: Utilizes modern C++ features for better performance and safety.
- **Lightweight**: Minimal overhead for maximum efficiency.

## Installation
To get started with Disruptor C++, follow these steps:

1. Clone the repository:
   ```bash
   git clone https://github.com/Kashemar2025/disruptor_cpp.git
   ```

2. Navigate to the project directory:
   ```bash
   cd disruptor_cpp
   ```

3. Build the project using your preferred build system (CMake is recommended):
   ```bash
   mkdir build
   cd build
   cmake ..
   make
   ```

4. Once built, you can download the latest release from [here](https://github.com/Kashemar2025/disruptor_cpp/releases) and execute the binary.

## Usage
Using Disruptor C++ is straightforward. Below is a simple example to demonstrate how to set up and use the library.

### Basic Example
```cpp
#include "disruptor.h"

class Event {
public:
    int value;
};

int main() {
    // Create a disruptor
    disruptor::Disruptor<Event> disruptor(1024);

    // Start the disruptor
    disruptor.start();

    // Publish an event
    disruptor.publish([](Event& event) {
        event.value = 42;
    });

    // Shutdown the disruptor
    disruptor.shutdown();
    return 0;
}
```

### Advanced Usage
For more complex scenarios, you can use custom event handlers and configure the disruptor to suit your needs. Check the examples folder in the repository for more advanced usage patterns.

## Examples
Explore the `examples` directory in this repository for more in-depth examples. These examples demonstrate various use cases of the Disruptor pattern, including:

- Event processing
- Message queuing
- Performance benchmarks

## Contributing
Contributions are welcome! If you want to help improve Disruptor C++, please follow these steps:

1. Fork the repository.
2. Create a new branch for your feature or bug fix.
3. Make your changes and commit them.
4. Push your changes to your forked repository.
5. Create a pull request.

Please ensure that your code adheres to the existing style and includes appropriate tests.

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Contact
For any questions or suggestions, feel free to reach out to me through GitHub. 

You can also visit the [Releases](https://github.com/Kashemar2025/disruptor_cpp/releases) section for updates and new features.

![Disruptor Pattern](https://miro.medium.com/max/1200/1*CRg3hR9_vL6QvYgFz-9ZxA.png)

## Acknowledgments
Special thanks to the original creators of the LMAX Disruptor and the open-source community for their contributions.

## Additional Resources
- [LMAX Disruptor Documentation](https://lmax-exchange.github.io/disruptor/)
- [C++20 Features](https://en.cppreference.com/w/cpp/20)

Feel free to explore, contribute, and utilize Disruptor C++ in your projects!