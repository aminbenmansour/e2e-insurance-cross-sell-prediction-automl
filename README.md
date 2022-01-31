# e2e-automl-cross-sell-prediction

# :warning: Disclaimer

**:warning: This is not my idea neither my work**, instead of forking this [repo](https://github.com/kennethleungty/End-to-End-AutoML-Insurance), I wanted to follow along step by step with the help of this [article](https://towardsdatascience.com/end-to-end-automl-train-and-serve-with-h2o-mlflow-fastapi-and-streamlit-5d36eedfe606).

Special thanks to the original author. mr. [Kenneth Leung](https://www.linkedin.com/in/kennethleungty/) for his valuable writings and contributions. Please consider supporting him and giving his [data science portfolio](https://github.com/kennethleungty) a look.

Please consider 

# introduction

This project aims to make cross-selling more efficient and targeted by building an ML pipeline to **identify health insurance customers interested in purchasing additional vehicle insurance**.

# toolkits overview

- **H2O AutoML**

     [H2O](https://docs.h2o.ai/h2o/latest-stable/h2o-docs/welcome.html) is an open-source, distributed, and scalable platform that enables users to easily build and productionalize ML models in enterprise environments.

     One of H2O’s key features is [H2O AutoML](https://docs.h2o.ai/h2o/latest-stable/h2o-docs/automl.html), a service that automates the ML workflow, including the automatic training and tuning of multiple models.

    This automation allows teams to focus on other vital components such as data preprocessing, feature engineering, and model deployment.
- **MLflow**
 
    [MLflow](https://mlflow.org/) is an open-source platform for managing ML lifecycles, including experimentation, deployment, and creation of a central model registry.

    The [MLflow Tracking](https://www.mlflow.org/docs/latest/tracking.html) component is an API that **logs and loads the parameters, code versions, and artifacts** from ML model experiments.

    MLflow also comes with a *mlflow.h2o* API module that integrates H2O AutoML runs with MLflow tracking.
- **FastAPI**

    [FastAPI](https://fastapi.tiangolo.com/) is a fast and highly performant web framework for building APIs in Python. It is designed to be user-friendly, intuitive, and production-ready.

    The purpose of deploying our ML model as a FastAPI endpoint is to readily retrieve prediction results after parsing our test data into the API.
- **Streamlit**

    [Streamlit](https://streamlit.io/) is an open-source app framework that turns data scripts into shareable web apps within minutes. It helps create user-friendly front-end interfaces for both technical and non-technical users to interact with.

    The user interface allows us to upload data to the backend pipeline via the FastAPI endpoint and then download predictions with a click of the mouse.
