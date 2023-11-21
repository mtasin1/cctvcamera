
<html lang="en">
<head>
  <meta charset="UTF-8"></meta>
  <meta content="width=device-width, initial-scale=1.0" name="viewport"></meta>
  <title>Psychologist-style Stress Assessment</title>
 <style>
    body {
      font-family: Arial, sans-serif;
      margin: 20px;
    }
    label {
      display: block;
      margin-bottom: 8px;
    }
    body {
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  margin: 20px;
  background-color: #f5f5f5;
}

h1 {
  color: #333;
}

form {
  background-color: #fff;
  padding: 20px;
  border-radius: 8px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}

label {
  display: block;
  margin-bottom: 8px;
  color: #555;
}

select,
input {
  width: 100%;
  padding: 10px;
  margin-bottom: 16px;
  border: 1px solid #ccc;
  border-radius: 4px;
  box-sizing: border-box;
  color: black;
}

button {
  background-color: #4caf50;
  color: #fff;
  padding: 10px 15px;
  border: none;
  border-radius: 4px;
  cursor: pointer;
}

button:hover {
  background-color: #45a049;
}

#result {
  margin-top: 20px;
  padding: 15px;
  border-radius: 8px;
  background-color: black;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}

#result h2 {
  color: #333;
}

 
    /* Your CSS styles here */
  </style>
</head>
<body>

  <h1>Psychologist-style Stress Assessment</h1>

  <form id="stressAssessment">
    <label for="workload">How would you rate the intensity of your current workload?</label>
    <select id="workload">
      <option value="1">Very low</option>
      <option value="2">Low</option>
      <option value="3">Moderate</option>
      <option value="4">High</option>
      <option value="5">Very high</option>
    </select>

    <label for="relationships">How satisfied are you with your personal relationships?</label>
    <select id="relationships">
      <option value="1">Very satisfied</option>
      <option value="2">Satisfied</option>
      <option value="3">Neutral</option>
      <option value="4">Dissatisfied</option>
      <option value="5">Very dissatisfied</option>
    </select>

    <label for="selfCare">How often do you engage in self-care activities (e.g., hobbies, relaxation)?</label>
    <select id="selfCare">
      <option value="1">Very often</option>
      <option value="2">Often</option>
      <option value="3">Occasionally</option>
      <option value="4">Rarely</option>
      <option value="5">Never</option>
    </select>

    <label for="copingSkills">How effective do you find your coping skills in managing stress?</label>
    <select id="copingSkills">
      <option value="1">Very effective</option>
      <option value="2">Effective</option>
      <option value="3">Moderate</option>
      <option value="4">Ineffective</option>
      <option value="5">Very ineffective</option>
    </select>

    <label for="lifeSatisfaction">How satisfied are you with your overall life?</label>
    <select id="lifeSatisfaction">
      <option value="1">Very satisfied</option>
      <option value="2">Satisfied</option>
      <option value="3">Neutral</option>
      <option value="4">Dissatisfied</option>
      <option value="5">Very dissatisfied</option>
    </select>

    <label for="resilience">How resilient do you consider yourself in facing life's challenges?</label>
    <select id="resilience">
      <option value="1">Very resilient</option>
      <option value="2">Resilient</option>
      <option value="3">Moderate</option>
      <option value="4">Not very resilient</option>
      <option value="5">Not resilient at all</option>
    </select>
    <label for="relaxation">Do you practice relaxation techniques (e.g., meditation, deep breathing)?</label>
    <select id="relaxation">
      <option value="1">Yes, regularly</option>
      <option value="2">Occasionally</option>
      <option value="3">No</option>
    </select>
 <label for="nutrition">How would you describe your nutritional habits?</label>
    <select id="nutrition">
      <option value="1">Healthy</option>
      <option value="2">Moderate</option>
      <option value="3">Unhealthy</option>
    </select>
       <label for="workLifeBalance">How would you rate your work-life balance?</label>
    <select id="workLifeBalance">
      <option value="1">Good</option>
      <option value="2">Fair</option>
      <option value="3">Poor</option>
    </select>

    <label for="exercise">Do you engage in regular exercise?</label>
    <select id="exercise">
      <option value="1">Yes, regularly</option>
      <option value="2">Occasionally</option>
      <option value="3">No</option>
    </select>
    <label for="sleepQuality">How would you rate the quality of your sleep?</label>
    <select id="sleepQuality">
      <option value="1">Good</option>
      <option value="2">Fair</option>
      <option value="3">Poor</option>
    </select>

    <label for="lifeEvents">Have you recently experienced significant life events (positive or negative)?</label>
    <select id="lifeEvents">
      <option value="1">No</option>
      <option value="2">Some</option>
      <option value="3">Many</option>
    </select>
     <label for="height">Height (cm):</label>
    <input id="height" required="" type="number" />

    <label for="weight">Weight (kg):</label>
    <input id="weight" required="" type="number" />

    <label for="age">Age:</label>
    <input id="age" required="" type="number" />

    <label for="gender">Gender:</label>
    <select id="gender">
      <option value="male">Male</option>
      <option value="female">Female</option>
    </select>

    <label for="exerciseFrequency">How often do you engage in cardiovascular exercise per week?</label>
    <select id="exerciseFrequency">
      <option value="0">Rarely or Never</option>
      <option value="1">1-2 times a week</option>
      <option value="2">3-4 times a week</option>
      <option value="3">5 or more times a week</option>
    </select>
    <label for="submit"></label>
    <button onclick="calculateStressLevel()" type="button">Submit</button>
  </form>

  <div id="result"></div>

  <script>
    function calculateStressLevel() {
      // Get values from the form
      var workload = parseInt(document.getElementById('workload').value);
      var relationships = parseInt(document.getElementById('relationships').value);
      var selfCare = parseInt(document.getElementById('selfCare').value);
      var copingSkills = parseInt(document.getElementById('copingSkills').value);
      var lifeSatisfaction = parseInt(document.getElementById('lifeSatisfaction').value);
      var resilience = parseInt(document.getElementById('resilience').value);
      var sleepQuality = parseInt(document.getElementById('sleepQuality').value);
      var lifeEvents = parseInt(document.getElementById('lifeEvents').value);
      var workLifeBalance = parseInt(document.getElementById('workLifeBalance').value);
      var exercise = parseInt(document.getElementById('exercise').value);
      var nutrition = parseInt(document.getElementById('nutrition').value);
      var relaxation = parseInt(document.getElementById('relaxation').value);
 
      var exerciseFrequency = parseInt(document.getElementById('exerciseFrequency').value);

      var bmi = weight / ((height / 100) * (height / 100));

      var bmr;
      if (gender === 'male') {
        bmr = 10 * weight + 6.25 * height - 5 * age + 5;
      } else {
        bmr = 10 * weight + 6.25 * height - 5 * age - 161;
      }

      // Calculate total stress level
      var totalStressLevel = workload + relationships + selfCare + copingSkills +
                            lifeSatisfaction + resilience+sleepQuality+lifeEvents+workLifeBalance+exercise+nutrition+relaxation+exerciseFrequency;

      // Display the result
      var resultDiv = document.getElementById('result');
      resultDiv.innerHTML = '<h2>Stress Level Assessment Result</h2>';
      resultDiv.innerHTML += '<p>Total Stress Level: ' + totalStressLevel + ' out of 56</p>';
 resultDiv.innerHTML += '<p>BMI: ' + bmi.toFixed(2) + '</p>';
      resultDiv.innerHTML += '<p>BMR: ' + bmr.toFixed(2) + ' calories/day</p>';
      // Provide a basic interpretation (customize based on your stress level criteria)
       
      if (totalStressLevel <= 20) {
        resultDiv.innerHTML += '<p>Your stress level is low. Keep up the good work!</p>';
      } else if (totalStressLevel <= 40) {
        resultDiv.innerHTML += '<p>Your stress level is moderate. Consider focusing on self-care and coping strategies.Here are some strategies that may help you manage and reduce stress:    <br>Identify Stressors:<br>Recognize the sources of stress in your life. Understanding what causes stress can help you address those factors more effectively.<br>Time Management:<br>Prioritize tasks and manage your time effectively. Break larger tasks into smaller, more manageable steps.<br>Healthy Lifestyle:<br>Adopt a healthy lifestyle with regular exercise, balanced nutrition, and sufficient sleep. Physical activity can help reduce stress hormones and improve mood.<br>Mindfulness and Relaxation Techniques:<br>Practice mindfulness meditation, deep breathing, or progressive muscle relaxation to help calm your mind and reduce stress.<br>Social Support:<br>Connect with friends, family, or support groups. Sharing your feelings and experiences can provide emotional support.<br>Set Realistic Goals:<br>Set achievable and realistic goals. Unrealistic expectations can contribute to stress.<br>Learn to Say No:<br>Understand your limits and do not hesitate to say no to additional responsibilities if you are already overwhelmed.<br>Hobbies and Leisure Activities:<br>Engage in activities you enjoy. Hobbies and leisure activities can provide a break from stress and contribute to a sense of fulfillment.<br>Positive Thinking:<br>Challenge negative thoughts and focus on positive aspects of situations. A positive outlook can help reduce stress.<br>Limit Stimulants:<br>Reduce the consumption of stimulants like caffeine and nicotine, especially in the evening, to promote better sleep.<br>Seek Professional Help:<br>If stress becomes overwhelming, consider seeking professional help from a therapist or counselor. They can provide strategies tailored to your individual needs.<br>Regular Check-ins:<br>Regularly assess your stress levels and adjust your strategies as needed. Its essential to be proactive in managing stress rather than waiting until it becomes overwhelming.Remember that everyone is different, so its important to find strategies that work best for you. </p>';
 } else {
        resultDiv.innerHTML += '<p>Your stress level is high. It may be beneficial to seek support and develop effective coping skills.<br> Consider focusing on self-care and coping strategies.Here are some strategies that may help you manage and reduce stress:    <br>Identify Stressors:<br>Recognize the sources of stress in your life. Understanding what causes stress can help you address those factors more effectively.<br>Time Management:<br>Prioritize tasks and manage your time effectively. Break larger tasks into smaller, more manageable steps.<br>Healthy Lifestyle:<br>Adopt a healthy lifestyle with regular exercise, balanced nutrition, and sufficient sleep. Physical activity can help reduce stress hormones and improve mood.<br>Mindfulness and Relaxation Techniques:<br>Practice mindfulness meditation, deep breathing, or progressive muscle relaxation to help calm your mind and reduce stress.<br>Social Support:<br>Connect with friends, family, or support groups. Sharing your feelings and experiences can provide emotional support.<br>Set Realistic Goals:<br>Set achievable and realistic goals. Unrealistic expectations can contribute to stress.<br>Learn to Say No:<br>Understand your limits and do not hesitate to say no to additional responsibilities if you are already overwhelmed.<br>Hobbies and Leisure Activities:<br>Engage in activities you enjoy. Hobbies and leisure activities can provide a break from stress and contribute to a sense of fulfillment.<br>Positive Thinking:<br>Challenge negative thoughts and focus on positive aspects of situations. A positive outlook can help reduce stress.<br>Limit Stimulants:<br>Reduce the consumption of stimulants like caffeine and nicotine, especially in the evening, to promote better sleep.<br>Seek Professional Help:<br>If stress becomes overwhelming, consider seeking professional help from a therapist or counselor. They can provide strategies tailored to your individual needs.<br>Regular Check-ins:<br>Regularly assess your stress levels and adjust your strategies as needed. Its essential to be proactive in managing stress rather than waiting until it becomes overwhelming.Remember that everyone is different, so its important to find strategies that work best for you. </p>';
      }
    }
  </script>

</body>
</html>
