# REST API

This project provides a Django-based REST API for managing user profiles. It includes endpoints for user profile creation, retrieval, updating, and deletion.

## Project Structure

- **`profiles_api/`**: Contains the core API logic, including models, serializers, views, and URLs.
- **`profiles_project/`**: Contains Django project settings, URLs, and WSGI configurations.
- **`deploy/`**: Deployment configurations, including Nginx and Supervisor configurations, setup scripts, and virtual machine setup.
- **`requirements/`**: Lists the Python packages required for the project.

## Features

- **User Profile Management**: CRUD operations for user profiles.
- **Feed API**: Additional endpoint for profile feed.

## Setup & Deployment

1. **Setup VM & Django**:
   - Use Vagrant for VM setup. Configure Django with `Vagrantfile` and `setup.sh`.

2. **Deployment Configuration**:
   - **Nginx**: `nginx_profiles_api.conf`
   - **Supervisor**: `supervisor_profiles_api.conf`
   - **Scripts**: `setup.sh`, `update.sh` for deployment automation.

3. **Install Dependencies**:
   - Install Python dependencies from `requirements`.

4. **Run Migrations**:
   - Apply database migrations using Django management commands.

5. **Start Server**:
   - Start the Django development server or configure for production using the provided deployment files.

## API Endpoints

- **Profiles**:
  - `GET /profiles/` - List all profiles
  - `POST /profiles/` - Create a new profile
  - `GET /profiles/{id}/` - Retrieve a profile by ID
  - `PUT /profiles/{id}/` - Update a profile by ID
  - `DELETE /profiles/{id}/` - Delete a profile by ID

- **Feed API**:
  - Additional endpoints for feed data related to user profiles.

## Development

- **Local Development**: Use `manage.py` for local development.
- **Testing**: Unit tests located in `profiles_api/tests.py`.

## Logging

- **Setup Logging**: Configured to capture detailed execution logs.

## Contributing

- **Testing**: Ensure new features are covered by tests.
