<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Streamlit Spiral Visualization App with Docker</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            line-height: 1.6;
            margin: 20px;
            padding: 0;
            background-color: #f9f9f9;
            color: #333;
        }
        h1, h2, h3 {
            color: #2c3e50;
        }
        code {
            background-color: #eaeaea;
            padding: 2px 5px;
            border-radius: 3px;
            font-family: "Courier New", Courier, monospace;
        }
        pre {
            background-color: #f4f4f4;
            padding: 10px;
            border-radius: 5px;
            overflow-x: auto;
        }
        a {
            color: #3498db;
            text-decoration: none;
        }
        a:hover {
            text-decoration: underline;
        }
        .section {
            margin-bottom: 30px;
        }
        .section h2 {
            border-bottom: 2px solid #3498db;
            padding-bottom: 5px;
        }
    </style>
</head>
<body>

    <h1>Streamlit Spiral Visualization App with Docker</h1>
    <p>Welcome to the <strong>Streamlit Spiral Visualization App</strong>! This project showcases an interactive Python application built with <strong>Streamlit</strong> that allows you to visualize and customize a spiral. The app is Dockerized for easy deployment and consistent behavior across different environments.</p>

    <div class="section">
        <h2>🌟 Features</h2>
        <ul>
            <li><strong>Interactive Controls</strong>: Use sliders to adjust the number of points and turns in the spiral.</li>
            <li><strong>Dynamic Visualization</strong>: Watch the spiral update in real-time as you tweak the parameters.</li>
            <li><strong>Dockerized Application</strong>: The app is containerized using Docker, ensuring portability and ease of deployment.</li>
            <li><strong>Responsive Design</strong>: The app is designed to work seamlessly across different devices and screen sizes.</li>
        </ul>
    </div>

    <div class="section">
        <h2>🚀 Technologies Used</h2>
        <ul>
            <li><strong>Python 3</strong>: The core programming language for this app.</li>
            <li><strong>Streamlit</strong>: A powerful framework for building interactive web applications.</li>
            <li><strong>Altair</strong>: A declarative statistical visualization library for Python, used to render the spiral.</li>
            <li><strong>Pandas</strong>: Used for data manipulation and handling data frames.</li>
            <li><strong>Docker</strong>: Containerizes the app for consistent behavior across environments.</li>
            <li><strong>NumPy</strong>: Used for mathematical computations to generate the spiral.</li>
        </ul>
    </div>

    <div class="section">
        <h2>⚙ Prerequisites</h2>
        <p>Before running the application, ensure you have the following installed on your local machine:</p>
        <ul>
            <li><strong>Docker</strong>: To build and run the app inside a container. Follow the official <a href="https://docs.docker.com/get-docker/" target="_blank">Docker Installation Guide</a> if you don't have it installed.</li>
            <li><strong>Git</strong>: To clone the repository.</li>
        </ul>
    </div>

    <div class="section">
        <h2>🛠 Getting Started</h2>
        <p>Follow these steps to set up and run the application:</p>

        <h3>Step 1: Clone the Repository</h3>
        <p>Clone the repository to your local machine:</p>
        <pre><code>git clone https://github.com/BhavyaDhimxn/container-experiments.git
cd Docker_Practices</code></pre>

        <h3>Step 2: Create a <code>requirements.txt</code> File</h3>
        <p>Ensure the project directory includes a <code>requirements.txt</code> file with the following dependencies:</p>
        <pre><code>streamlit
altair
pandas
numpy</code></pre>

        <h3>Step 3: Build the Docker Image</h3>
        <p>Build the Docker image from the project directory:</p>
        <pre><code>docker build -t streamlit-spiral-app .</code></pre>
        <p>This will use the <code>Dockerfile</code> to create an image named <code>streamlit-spiral-app</code>.</p>

        <h4>Verify the Docker Image</h4>
        <p>After building the image, verify its creation:</p>
        <ul>
            <li><strong>Using Docker Desktop</strong>: Check the <strong>Images</strong> section for the <code>streamlit-spiral-app</code> image.</li>
            <li><strong>Using the Command Line</strong>:
                <pre><code>docker images</code></pre>
                Look for the <code>streamlit-spiral-app</code> image in the list.
            </li>
        </ul>

        <h3>Step 4: Run the Docker Container</h3>
        <p>Start the app inside a Docker container:</p>
        <pre><code>docker run -p 8501:8501 streamlit-spiral-app</code></pre>
        <p>This command maps port <code>8501</code> inside the container to port <code>8501</code> on your local machine.</p>

        <h3>Step 5: Access the Streamlit App</h3>
        <p>Open your browser and navigate to:</p>
        <pre><code>http://localhost:8501</code></pre>
        <p>You should now see the Streamlit app, where you can interactively adjust the spiral's parameters.</p>
    </div>

    <div class="section">
        <h2>🌀 How the App Works</h2>
        <h3>Interactive Sliders</h3>
        <ul>
            <li><strong>Number of Points in Spiral</strong>: Controls the density of points in the spiral.</li>
            <li><strong>Number of Turns in Spiral</strong>: Adjusts the number of full rotations the spiral makes.</li>
        </ul>

        <h3>Real-Time Visualization</h3>
        <p>As you adjust the sliders, the spiral is dynamically updated in real-time using <strong>Altair</strong> for rendering.</p>

        <h3>Under the Hood</h3>
        <ul>
            <li>The app generates spiral points using polar coordinates.</li>
            <li>The <code>x</code> and <code>y</code> positions are calculated using trigonometric functions (<code>np.cos</code> and <code>np.sin</code>).</li>
            <li>The data is visualized using <strong>Altair</strong> as a scatter plot.</li>
        </ul>
    </div>

    <div class="section">
        <h2>💻 Code Explanation</h2>
        <h3>NamedTuple for Points</h3>
        <p>The spiral points are stored as <code>Point</code> objects using Python’s <code>namedtuple</code>:</p>
        <pre><code>Point = namedtuple('Point', ['x', 'y'])</code></pre>

        <h3>Generating Spiral Data</h3>
        <p>The spiral is generated using the following logic:</p>
        <pre><code>def generate_spiral(num_points, num_turns):
    data = []
    for i in range(num_points):
        angle = 2 * np.pi * num_turns * (i / num_points)
        radius = i / num_points
        x = radius * np.cos(angle)
        y = radius * np.sin(angle)
        data.append(Point(x, y))
    return data</code></pre>

        <h3>Streamlit Visualization</h3>
        <p>The data is passed to <strong>Altair</strong> for visualization:</p>
        <pre><code>chart = alt.Chart(spiral_df).mark_circle(size=3).encode(
    x='x',
    y='y'
).properties(
    width=600,
    height=600
)</code></pre>
    </div>

    <div class="section">
        <h2>🛠 Troubleshooting</h2>
        <p>If you encounter issues, follow these steps:</p>
        <ol>
            <li><strong>Check Docker Logs</strong>:
                <pre><code>docker logs &lt;container_id&gt;</code></pre>
            </li>
            <li><strong>Verify Dependencies</strong>:
                Ensure the <code>requirements.txt</code> file is correctly copied into the Docker image and all dependencies are installed.
            </li>
            <li><strong>Port Conflicts</strong>:
                Ensure port <code>8501</code> is not being used by another application.
            </li>
        </ol>
    </div>

    <div class="section">
        <h2>🤝 Contributing</h2>
        <p>We welcome contributions to improve this project! Here’s how you can contribute:</p>
        <ol>
            <li>Fork the repository.</li>
            <li>Create a new branch for your changes.</li>
            <li>Make your changes and commit them.</li>
            <li>Push your changes to your forked repository.</li>
            <li>Open a pull request to merge your changes into the main repository.</li>
        </ol>
    </div>

    <div class="section">
        <h2>🎉 Happy Coding!</h2>
    </div>

</body>
</html>