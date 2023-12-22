<div align="center">
    <a href="https://turbostrapi.vercel.app/">
        <img height="70" src="./logo.png" />
    </a>
    <br />
    <br />
    <strong>Dockerized TurboStrapi with Traefik</strong>
    <br />
    <br />
</div>

Before starting, ensure you have Docker, OpenSSL, and Git installed on your system. Basic knowledge of Docker and Traefik is also required.

## 🛠️ Setup Traefik

Setup the [Dockerized Traefik](https://github.com/sawden/traefik-base) before proceeding.

## 📥 Clone this Project

```bash
git clone git@github.com:sawden/traefik-turbostrapi.git /opt/containers/EXAMPLE_PROJECT
```

#### ⚙️ Configure Docker Variables

```bash
# Copy the sample env
cp /opt/containers/EXAMPLE_PROJECT/.env.example /opt/containers/EXAMPLE_PROJECT/.env
# Edit the .env and replace 'example' data
nano /opt/containers/EXAMPLE_PROJECT/.env
# Generate 'JWT_SECRET', 'ADMIN_JWT_SECRET', 'API_TOKEN_SALT' and 'TRANSFER_TOKEN_SALT' with
openssl rand -base64 48
```

#### 📂 Setting Up TurboStrapi Project

```bash
# Create data
mkdir /opt/containers/EXAMPLE_PROJECT/data
# Clone a TurboStrapi project of choice as "project"
git clone git@github.com:sawden/turbostrapi.git /opt/containers/EXAMPLE_PROJECT/data/project
```

## 🚀 Start the Project

```bash
docker-compose up -d
```

## 📚 Documentation

<strong>See the official documentation for installation and support instructions [here](https://turbostrapi.vercel.app/deployment#traefik).</strong>

## 💬 Support and Contributions

For support or contributions, create an issue on GitHub or contact us directly.