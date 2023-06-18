# Exp08-webdev
# BMI calculator
## Aim:
To develop a BMI calculator.
## Algorithm:
1. Code all the necessary Css elements.
2. And connect it with the HTML page.
3. Then execute it.
4. Display the results.
## Code:
```
HTML

import React, { useState } from 'react';

function BMICalculator() {
  const [weight, setWeight] = useState('');
  const [height, setHeight] = useState('');
  const [bmi, setBMI] = useState(null);

  const calculateBMI = () => {
    const heightInMeters = height / 100;    
    const bmiValue = weight / (heightInMeters * heightInMeters);
    setBMI(bmiValue.toFixed(2));
  };

  return (
    <div>
      <h2>BMI Calculator</h2>
      <div>
        <label htmlFor="weight">Weight (kg):</label>
        <input
          type="text"
          id="weight"
          value={weight}
          onChange={(e) => setWeight(e.target.value)}
        />
      </div>
      <div>
        <label htmlFor="height">Height (cm):</label>
        <input
          type="text"
          id="height"
          value={height}
          onChange={(e) => setHeight(e.target.value)}
        />
      </div>
      <button onClick={calculateBMI}>Calculate BMI</button>
      {bmi && <p>Your BMI is: {bmi}</p>}
    </div>
  );
}

export default BMICalculator;
```

## Output:
![image](https://github.com/Archana2003-Jkumar/Exp08-webdev/assets/93427594/4384671a-b37c-4423-a9c8-59282bd5bdc9)
## Result:
Thus the code has been implemented successfully.
