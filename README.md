# **🗓️ NextDate: Find Common Availability**

NextDate is a simple, mobile-friendly web application designed to help groups of people find common available dates for meetings, events, or gatherings. Users can add multiple participants and specify their individual availability (single dates or date ranges). The application then automatically calculates and displays the dates that are common to all participants. Additionally, it offers a "Projected Availability" feature that uses a heuristic to estimate the likelihood of all participants being available on any selected date, taking into account weekday effects.

## **✨ Features**

* **Add Multiple Participants**: Easily add names of all individuals involved.  
* **Flexible Date Entry**: For each person, specify available dates as single days or continuous ranges.  
* **Real-time Common Dates**: Instantly see which dates are available for *everyone* based on explicit entries.  
* **Intuitive Date Picker**: Utilizes Flatpickr for seamless date selection.  
* **Projected Availability Heuristic**:  
  * For any selected date, it first checks if it's a known common date.  
  * If not, it calculates a projected availability percentage for each person based on their historical availability for that specific day of the week.  
  * It then calculates a joint probability of all participants being available on that date.  
  * A clear summary (green for \>50% joint probability, red for \<=50%) indicates the overall likelihood of collective availability.  
* **Responsive Design**: Built with Tailwind CSS for optimal viewing and usability across various devices (mobile, tablet, desktop).  
* **Sophisticated Typography**: Uses 'Playfair Display' for headings and 'Lato' for body text for an elegant look.  
* **Fun Icons**: Integrated Font Awesome icons enhance the user interface.  
* **In-Memory Data Storage**: All data is stored in the browser's memory for simplicity (data will not persist on page refresh/close).

## **🚀 How to Use**

1. **Open the Application**: Simply open the index.html file in your web browser.  
2. **Add People**:  
   * In the "Add New Person" section, type a person's name into the input field.  
   * Press Enter or click the "Add Person" button. A new card for that person will appear.  
3. **Add Availability**:  
   * For each person's card, click the "Select Date(s)" button.  
   * A calendar picker will appear. Select a single date or a range of dates.  
   * As soon as you select the date(s), they will be added to the person's availability list, and the "Common Available Dates" will automatically update.  
4. **Remove Dates/People**:  
   * To remove an individual date from a person's list, click the × button next to that date.  
   * To remove an entire person, click the large × button at the top right of their card.  
5. **Check Projected Availability**:  
   * In the "Projected Availability" section, click the "Select a Date for Projection" input field.  
   * Choose any date from the calendar.  
   * The application will immediately display the projected availability for that date, including a summary and individual probabilities.

## **💡 Projected Availability Heuristic**

The "Projected Availability" feature uses a simple heuristic to estimate availability for dates that are not explicitly marked as common. For a selected date, it calculates each person's probability of being available on that specific day of the week (e.g., a Tuesday).

The individual probability for a person for a given weekday is:

P(Person available on selected weekday)=Total number of that weekday within person’s overall provided date rangeNumber of times person is explicitly available on that weekday​  
The overall joint probability of all participants being available is then calculated by multiplying their individual probabilities (assuming independence for simplicity).

A summary line at the top of the "Projected Availability" section provides quick feedback:

* **Green**: If the joint probability is greater than 50%.  
* **Red**: If the joint probability is 50% or less.

## **🛠️ Technologies Used**

* **HTML5**: Structure of the web page.  
* **Tailwind CSS**: For responsive and utility-first styling.  
* **JavaScript (ES Modules)**: Core logic and interactivity.  
* **Flatpickr**: A lightweight and powerful date picker.  
* **Font Awesome**: For various icons used throughout the application.

## **🤝 Contribution**

Feel free to fork this repository, suggest improvements, or contribute to enhance the functionality of NextDate\!

© 2025 NextDate. Built with ❤️ by Arun.
