# Queue Cure '26

A beginner-friendly full-stack healthcare queue management system built with vanilla HTML, CSS, JavaScript, Node.js, Express.js, and Socket.IO.

## Features

### Landing Page (index.html)
- Modern healthcare-themed interface
- Navigation to Receptionist Dashboard and Patient Waiting Room
- Feature highlights and system overview

### Receptionist Dashboard (receptionist.html)
- **Add Patient**: Add new patients to the queue with auto-generated token numbers starting from 101
- **Queue Management**: View all patients currently in the queue
- **Call Next Token**: Call the next patient in line
- **Current Token Display**: Shows which patient is currently being served
- **Settings**: Configure average consultation time for wait time calculations
- **Real-time Updates**: Instant synchronization with patient display

### Patient Waiting Room (patient.html)
- **Current Token Display**: Shows the token number currently being served
- **Tokens Ahead**: Number of patients waiting before you
- **Estimated Wait Time**: Calculated based on queue position and average consultation time
- **Live Updates**: Automatic updates when receptionist calls next token (no page refresh needed)
- **Upcoming Tokens**: Preview of next tokens to be called

## Technology Stack

- **Frontend**: HTML5, CSS3, Vanilla JavaScript
- **Backend**: Node.js, Express.js
- **Real-time Communication**: Socket.IO
- **Styling**: Modern CSS with gradients and animations

## Installation

1. Install dependencies:
```bash
npm install
```

2. Start the server:
```bash
npm start
```

3. Open your browser and navigate to:
```
http://localhost:3000
```

## Usage

### For Receptionists:
1. Go to the landing page and click "Receptionist Dashboard"
2. Add patients by entering their name and clicking "Add to Queue"
3. Set the average consultation time in minutes
4. Click "Call Next Token" to serve the next patient
5. Monitor the queue in real-time

### For Patients:
1. Go to the landing page and click "Patient Waiting Room"
2. View your current token number and position in queue
3. See estimated wait time based on your position
4. Wait for your token number to be called

## Project Structure

```
/
├── public/
│   ├── index.html          # Landing page
│   ├── receptionist.html   # Receptionist dashboard
│   ├── patient.html        # Patient waiting room display
│   └── style.css           # Shared styles
├── server.js               # Express + Socket.IO server
├── package.json            # Dependencies and scripts
└── README.md              # Documentation
```

## Real-time Features

The application uses Socket.IO for real-time bidirectional communication:

- **Connection Status**: Shows live/offline status on all pages
- **Queue Updates**: When receptionist adds a patient, all displays update instantly
- **Token Calls**: When next token is called, patient display updates immediately
- **Settings Sync**: Consultation time changes sync across all connected clients

## Customization

### Styling
Edit `public/style.css` to customize:
- Colors (default: blue and white healthcare theme)
- Fonts
- Layout and spacing
- Animations

### Consultation Time
Default average consultation time is 10 minutes, adjustable from the receptionist dashboard.

### Token Numbers
Tokens start from 101 by default. Modify `nextTokenNumber` in `server.js` to change.

## Browser Compatibility

Works on all modern browsers:
- Chrome
- Firefox
- Safari
- Edge

## License

Open source - feel free to use and modify for your needs.

## Future Enhancements

Potential improvements:
- Multiple departments/queues
- SMS notifications for patients
- Historical data and analytics
- Print token functionality
- Multi-language support

---

**Queue Cure '26** - Streamlining Healthcare Experiences
