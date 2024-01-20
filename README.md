CPU SCHEDULING SIMULATOR

The concept of a CPU Scheduling Simulator emerges from the fundamental principles of operating systems, particularly focusing on how they manage and allocate CPU time to various running processes. At its core, an operating system's efficiency and effectiveness are significantly determined by its ability to manage multiple tasks, often simultaneously. This management involves determining the order and duration for which each process accesses the CPU, a decision-making process known as CPU scheduling. The CPU scheduling algorithms are pivotal in this process, as they dictate the sequence of process execution based on specific criteria, aiming to optimise various performance metrics like throughput, turnaround time, waiting time, and CPU utilisation.

Understanding these algorithms is not just crucial for system designers and computer scientists but also for students learning the intricacies of operating systems. However, the theoretical understanding of these algorithms can sometimes be abstract and challenging to grasp. This is where a CPU scheduling simulator comes into play. It serves as a practical, interactive tool that allows users—whether they are students, educators, or professionals—to visualize and comprehend how different scheduling algorithms operate in a dynamic, real-time environment.

The primary objective of this simulator is to provide a hands-on learning experience. By allowing users to create and manage a set of processes with varying arrival times, burst times, and other parameters, the simulator offers an immersive learning environment. Users can select different scheduling algorithms, such as First-Come, First-Served (FCFS), Shortest Job First (SJF), Priority Scheduling, and Round Robin, and observe how each algorithm manages the processes. This observation is crucial in understanding the strengths and weaknesses of each algorithm, providing insights into which algorithm might be best suited for a particular scenario. For instance, FCFS is straightforward but can lead to long waiting times, while SJF can minimize waiting time but might cause the problem of process starvation.

The development of a web-based CPU Scheduling Simulator. This simulator is designed to provide an interactive and educational platform for understanding and analyzing various CPU scheduling algorithms. The primary scope of the project includes:

Development of a Web-based Simulator: 

Creating an offline platform that is accessible and easy to use, providing a practical learning tool for students, educators, and professionals interested in operating systems and can easily solve their problems regarding CPU Scheduling Algorithms.

Implementation of Scheduling Algorithms:

 Integrating key CPU scheduling algorithms such as First-Come, First-Served (FCFS), Shortest Job First (SJF), Priority Scheduling, and Round Robin. These algorithms will form the core of the simulator, allowing users to explore and compare different scheduling strategies.

Interactive User Interface (UI): 

Developing a user-friendly interface that allows users to easily add and manage processes. This interface will enable the input of process details such as Process ID, Arrival Time, Burst Time, Quantum no. and Priority.
The simulator will boast several features to enhance user experience and learning:
•	Ensuring ease of use for inputting process details, thereby making the tool accessible to users with varying levels of expertise.
•	Allowing users to choose different scheduling algorithms and observe their behavior in real-time.
•	Showing immediate scheduling results, including key metrics like Waiting Time and Turnaround Time for each process.
•	Calculating and displaying average Waiting Time and Turnaround Time, providing insights into the efficiency of each algorithm.
•	Incorporating a Gantt Chart to visually represent the scheduling process, enhancing understanding through visual aids.
The methodology for this project will be grounded in robust web development practices:
Front-End Development: Utilizing HTML, CSS, and JavaScript to develop the front end of the simulator. These technologies are chosen for their flexibility, compatibility, and widespread use in web development and the main purpose of implementation in these frontend technologies are easy to implement and easy to understand.
Algorithm Implementation is Writing the logic for CPU scheduling algorithms in JavaScript, ensuring that they are accurately and efficiently executed.

A Fully Functional CPU Scheduling Simulator:

Completion of the project will result in a fully operational web-based simulator. This tool will accurately demonstrate various CPU scheduling algorithms, offering an interactive platform for users to input and manage process details, and observe the algorithms' performance in real time.
 
Enhanced Understanding of Scheduling Algorithms for Users:

The simulator will serve as an invaluable educational resource, significantly enhancing users' understanding of different CPU scheduling algorithms. Through direct interaction and experimentation with the tool, users will gain deeper insights into how these algorithms operate and affect key performance metrics like waiting time and turnaround time.

The CPU Scheduling Simulator project stands as a vital educational and practical tool, bridging theoretical knowledge with hands-on experience in the field of computer science. Its development marks a significant stride in the understanding and teaching of CPU scheduling, making complex concepts more accessible and comprehensible. This simulator is expected to have a profound impact on learning and comprehension in the domain of operating systems, benefiting students, educators, and professionals alike. Its implementation will not only enhance learning experiences but also foster a deeper appreciation and understanding of the intricacies involved in CPU scheduling within operating systems.

CPU SCHEDULING SIMULATOR PSEUDOCODE

Initialization:
1. Create an empty list named 'processes'.
2. Attach event listeners to 'Add Process', 'Calculate', and 'Clear Processes' buttons, and 'Algorithm Selector' dropdown.

Event Handlers:
1. Add Process:
   - On 'Add Process' button click:
     - Read Process ID, for all from input fields.
     - Validate inputs for numeric values.
     - If valid, add new process to 'processes' list with initial values.
     - Update display table with new process list.

2. Calculate Scheduling:
   - On 'Calculate' button click:
     - Read selected scheduling algorithm.
     - Reset previous calculations.
     - Call function for selected algorithm (FCFS, SJF, Priority, Round Robin).
     - Compute and display average waiting and turnaround times.
     - Update display table with calculated values.
 
3. Clear Processes:
   - On 'Clear Processes' button click:
     - Clear 'processes' list.
     - Reset displayed average times.
     - Update display table to show no processes.

Scheduling Algorithms:
1. First Come First Served (FCFS):
   - For each process in order:
     - Update waiting, turnaround, and completion times.

2. Shortest Job First (SJF):
   - Sort processes by burst time, then by arrival time if burst times equal.
   - Apply FCFS on sorted list.

3. Priority Scheduling:
   - Sort processes by priority.
   - Apply FCFS on sorted list.

4. Round Robin:
   - Initialize 'currentTime' and process queue with 'executedTime'.
   - Until all processes completed:
     - For each process in queue:
       - If process has remaining burst time and has arrived:
         - Allocate CPU time (min of remaining burst time or time quantum).
         - Update 'executedTime' and 'remainingBurstTime'.
         - If process completed, update completion, waiting, and turnaround times.
       - If no process ready, increment 'currentTime'.

Utility Functions:
1. Compute Averages:
   - Calculate average waiting and turnaround times from 'processes' list.

2. Update Table:
   - Clear and repopulate results table with current process data.

3. Handle Algorithm Change:
   - Show/hide inputs (Time Quantum, Priority) based on selected algorithm.
