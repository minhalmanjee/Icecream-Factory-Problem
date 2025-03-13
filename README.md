# Ice Cream Shop Simulation

## Technologies Used
- **C (Kernel Programming)**: Implemented the ice cream shop simulation using kernel threads and synchronization primitives.
- **Linux Kernel Modules**: The project is developed as a Linux kernel module.
- **Synchronization (Semaphores)**: Used semaphores to prevent race conditions and manage shared resources.
- **Multithreading (Kernel Threads)**: Simulated multiple customers using kernel threads.
- **Syscalls (System Calls)**: Implemented a custom system call for managing customer interactions.
- **Kernel Debugging (Printk)**: Used `printk` for logging and debugging within the kernel.

## Project Overview
This project simulates an ice cream shop with multiple customers using kernel threads. It manages ticket allocation, flavor selection, topping selection, and payment processing while ensuring synchronization using semaphores.

## Features
- **Ticket Allocation**: Customers obtain tickets to enter the shop.
- **Flavor Selection**: Customers select from three flavors with limited stock.
- **Topping Selection**: Customers can choose from two toppings.
- **Payment Processing**: The total bill is calculated, and revenue is updated.
- **Thread Synchronization**: Uses semaphores to prevent race conditions.
- **Logging**: Kernel messages provide insight into operations.

## Installation and Usage
1. Compile the module:
   ```sh
   make
   ```
2. Load the module:
   ```sh
   sudo insmod icecream.ko
   ```
3. Check logs:
   ```sh
   dmesg | tail -n 50
   ```
4. Remove the module:
   ```sh
   sudo rmmod icecream
   ```

## License
This project is licensed under the MIT License.

