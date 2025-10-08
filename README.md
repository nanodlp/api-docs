# API Documentation

The API documented herein is for the latest version of the NanoDLP 3D printing control system. As a system under active internal development, the specifications detailed in this Swagger/OpenAPI documentation are fluid and subject to revision at any time.

## 📁 Documentation Files

- **`swagger.json`** - Complete OpenAPI 2.0 specification in JSON format
- **`swagger.yaml`** - OpenAPI 2.0 specification in YAML format  

## 🔍 API Coverage

The documentation covers **231+ API endpoints** across all modules:

- **Web API** - Core printer control and management
- **Editor** - 3D model editing and manipulation
- **Debug** - Development and debugging utilities
- **Task Management** - Background job processing

## 🌐 How to View the Documentation

### Option 1: Online Swagger Editor (Recommended)
1. Go to [https://editor.swagger.io/](https://editor.swagger.io/)
2. Click "File" → "Import File"
3. Upload `docs/swagger.json` or `docs/swagger.yaml`
4. Explore the interactive API documentation

### Option 2: Local Swagger UI
```bash
# Install swag tool
go install github.com/swaggo/swag/cmd/swag@latest

# Serve documentation locally
swag serve -F swagger docs/swagger.json
```
Then open [http://localhost:8080/swagger/index.html](http://localhost:8080/swagger/index.html)

### Option 3: Redoc (Alternative UI)
```bash
# Install redoc-cli
npm install -g redoc-cli

# Generate and serve Redoc documentation
redoc-cli serve docs/swagger.json
```
Then open [http://localhost:8080](http://localhost:8080)

### Option 4: VS Code Extension
1. Install "OpenAPI (Swagger) Editor" extension
2. Open `docs/swagger.json` or `docs/swagger.yaml`
3. Use the built-in preview feature

## 📊 API Statistics

- **Total Endpoints**: 231+
- **Authentication**: Bearer Token
- **Base URL**: `http://localhost:8080`
- **Protocols**: HTTP, HTTPS
- **Response Formats**: JSON, HTML, Binary

## 🏷️ API Categories

- **Authentication** - User login and security
- **Plates** - Print job management
- **Slicing** - 3D model processing
- **Editor** - Model manipulation tools
- **Printer** - Hardware control
- **Debug** - Development utilities


## 🆘 Troubleshooting

**Q: Documentation shows only a few endpoints**
A: Ensure all route files have proper `@Summary` annotations and run the generation script with all flags.

**Q: Swagger UI shows errors**
A: Check that the JSON/YAML files are valid. Use an online validator to verify.

**Q: Missing type definitions**
A: Replace custom types with `map[string]interface{}` or define proper response models.

## 📚 Additional Resources

- [OpenAPI Specification](https://swagger.io/specification/)
- [Swagger UI Documentation](https://swagger.io/tools/swagger-ui/)
- [Redoc Documentation](https://redoc.ly/)
- [Echo Swagger Integration](https://github.com/swaggo/echo-swagger)
