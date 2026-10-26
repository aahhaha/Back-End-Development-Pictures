# Back-End-Development-Pictures

Flask REST API for the Pictures service in the IBM backend capstone.

## Environment Setup
- Repository created from the official IBM template.
- Local implementation verified with Python 3.12.14.
- Original lab setup script: `bin/setup.sh` (Linux Cloud IDE).
- Portable setup: `python -m venv .venv`, activate it, then `pip install -r requirements.txt`.

## Run and test
`flask --app backend run --port 8081`

`python -m pytest -v tests`

Endpoints: GET /health, GET /count, GET /picture, GET /picture/<id>, POST /picture, PUT /picture/<id>, DELETE /picture/<id>.
Data starts from backend/data/pictures.json and changes remain in memory until restart, as in the lab design.

## Container
`docker build -t pictures .`

`docker run --rm -p 8081:3000 pictures`
