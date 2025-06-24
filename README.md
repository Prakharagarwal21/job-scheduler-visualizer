# Job Scheduler Visualization

A web-based interactive tool to demonstrate and compare various job scheduling algorithms, including Greedy, Dynamic Programming (DP), Backtracking, and MultiQueue scheduling. The project visualizes scheduled jobs and their execution timelines using Chart.js.

---
## Folder Structure
RealTimeTaskOptimize/
├── index.html               # Main HTML page with UI and canvas for charts
├── styles.css               # CSS styles for layout and form elements
├── algorithms.js            # JavaScript implementation of scheduling algorithms
├── main.js                  # UI logic, event handlers, and chart visualization
└── README.md                # This documentation file

## Features

- Add jobs with customizable attributes:  
  - **ID** (string)  
  - **Deadline** (number)  
  - **Execution Time** (number)  
  - **Profit** (number)  
  - **Priority** (number)

- Choose among scheduling algorithms:  
  - Greedy (profit-based)  
  - Dynamic Programming (max profit with deadlines)  
  - Backtracking (exhaustive max profit)  
  - MultiQueue (priority-based with Round Robin for low priority)

- Visualize job execution timeline in an intuitive horizontal bar chart.

- Compare execution time and output of all algorithms side-by-side.

---

## How to Run

1. Download or clone this repository.

2. Make sure all files (`index.html`, `algorithms.js`, `main.js`, `styles.css`) are in the same folder.

3. Open `index.html` in a modern web browser (Chrome, Firefox, Edge).

4. Add job details in the form and click **Add Job**.

5. Select the scheduling algorithm from the dropdown.

6. Click **Run** to see the scheduling results and timeline visualization.

7. Use **Compare All** option to benchmark all algorithms' execution time and results.

---

## File Overview

- `index.html` — Main HTML page with UI and canvas for charts.

- `styles.css` — Basic styling for layout and form elements.

- `algorithms.js` — Scheduling algorithms implementation in JavaScript.

- `main.js` — UI handling, event listeners, and Chart.js visualization code.

---

## Scheduling Algorithms Implemented

- **Greedy:** Schedules jobs by descending profit and fits jobs before their deadlines.

- **Dynamic Programming:** Finds maximum profit schedule respecting deadlines using DP.

- **Backtracking:** Exhaustively searches all subsets to find max profit.

- **MultiQueue:**  
  - High priority jobs (priority ≥ 7) scheduled FCFS.  
  - Low priority jobs scheduled using a simulated Round Robin with quantum = 2 units.

---

## Dependencies

- [Chart.js](https://www.chartjs.org/) (loaded via CDN) for rendering timeline and execution time charts.

---

## Notes

- The timeline charts represent each job's execution duration on a horizontal axis with job IDs on the vertical axis.

- Input validation is minimal — please enter reasonable numeric values.

- Jobs added remain in memory until the page is refreshed.

---
