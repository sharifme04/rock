# Rock Paper Scissors: Score Display

A Flask game that counts how many rounds the player and the computer have won.

## Run it

```
pip install flask
python app.py
```

Then open http://127.0.0.1:5000

## What I changed

- `app.py`: added `user_score` and `computer_score`, updated them after each round, and included both in the JSON response from `/play`.
- `templates/index.html`: added `<div id="score">0:0</div>` inside the game container.

## What happens to the score after restarting the Flask server, and why?

The score goes back to 0:0. It is stored only in Python variables, which live in the server's memory. When the server stops, that memory is cleared, and when it starts again the variables are set to 0. To keep the score, it would have to be saved outside the program, for example in a JSON file or a database.
