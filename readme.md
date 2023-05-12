# PaTAT
# Overview

- [To build and run from source-code](#to-build-and-run-from-source-code)
  - [Frontend](#frontend)
  - [Backend](#backend)
- [To run in docker](#to-run-in-docker)
  - [Backend](#backend-1)
  - [Frontend](#frontend-1)
- [To run in docker-compose](#to-run-in-docker-compose)
- [To view API docs](#to-view-api-docs)

## Notes:

Currently uses Python 3.9

# To build and run from source-code

In two different terminals, do:

## Frontend

- cd into frontend
- `npm install --legacy-peer-deps`
- `npm start`

## Backend

- cd into backend
- create a new environment (for example, using miniconda or python3's venv at the command line, i.e., `python3 -m venv ./venv` and then `venv/bin/activate`)
- `pip install -r requirements.txt`
- `python -m spacy download en_core_web_sm`
- `uvicorn main:app --port 8080 --host 0.0.0.0`

# To run in docker

In two different terminals, do:

## Backend

- cd into backend
- `docker build -t patat-backend .`
- `docker run -p 8080:8080 patat-backend`

## Frontend

- cd into frontend
- `docker build -t patat-frontend .`
- `docker run -p 3000:3000 patat-frontend`

# To run in docker-compose

- install `docker-compose` if you don't have it installed
- `docker-compose up --build`

# To view API docs

- head to `http://localhost:8080/docs` after running the backend

# Reference
If you use our tools/code for your work, please cite the following paper:
Simret Araya Gebreegziabher, Zheng Zhang, Xiaohang Tang, Yihao Meng, Elena L. Glassman, and Toby Jia-Jun Li. 2023. PaTAT: Human-AI Collaborative Qualitative Coding with Explainable Interactive Rule Synthesis. In Proceedings of the 2023 CHI Conference on Human Factors in Computing Systems (CHI '23). https://doi.org/10.1145/3544548.3581352


