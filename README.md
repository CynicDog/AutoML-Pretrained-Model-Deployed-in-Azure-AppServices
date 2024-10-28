# AutoML-Best-Model-Deployed-in-Azure-AppServices

### Version Table

### Environment Variables 
- `BEST_MODEL_NAME`: `wheat_brake_11f3294kdb`
- `WS_NAME`: `inbrein-azure-ml-research-eunsang`
- `RG_NAME`: `inbrein-azure-ml-research`

## Steps 

### Download Best Model 

```bash
PS C> az ml job download --name $BEST_MODEL_NAME \
        --all --download-path /app/configs/downloaded_artifacts \
        --workspace-name $WS_NAME \
        --resource-group $RG_NAME 
```

### Create Conda Environment 
```bash
PS C:\app\configs\downloaded_artifacts\named-outputs\best_model> conda env create -f .\conda.yaml
```
