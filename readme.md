from flask import Flask, render_template, request

app = Flask(__name__)

@app.route('/')
def index():
    return render_template('index.html')

@app.route('/signup', methods=['GET', 'POST'])
def signup():
    if request.method == 'POST':
        # Handle form data here
        pass
    return render_template('signup.html')

if __name__ == '__main__':
    app.run(debug=True)
