# Επιστήμη Δεδομένων στο Cloud: Ο τρόπος "Azure ML SDK"

|![ Σχεδίαση από [(@sketchthedocs)](https://sketchthedocs.dev) ](../../sketchnotes/19-DataScience-Cloud.png)|
|:---:|
| Επιστήμη Δεδομένων στο Cloud: Azure ML SDK - _Σχεδίαση από [@nitya](https://twitter.com/nitya)_ |

Πίνακας περιεχομένων:

- [Επιστήμη Δεδομένων στο Cloud: Ο τρόπος "Azure ML SDK"]( #data-science-in-the-cloud-the-azure-ml-sdk-way)
  - [Προ-Διάλεξη Κουίζ](#προ-διάλεξη-κουίζ)
  - [1. Εισαγωγή](#1-εισαγωγή)
    - [1.1 Τι είναι το Azure ML SDK;](#11-τι-είναι-το-azure-ml-sdk)
    - [1.2 Έργο πρόβλεψης καρδιακής ανεπάρκειας και εισαγωγή δεδομένων](#12-έργο-πρόβλεψης-καρδιακής-ανεπάρκειας-και-εισαγωγή-δεδομένων)
  - [2. Εκπαίδευση μοντέλου με το Azure ML SDK](#2-εκπαίδευση-μοντέλου-με-το-azure-ml-sdk)
    - [2.1 Δημιουργία χώρου εργασίας Azure ML](#21-δημιουργία-χώρου-εργασίας-azure-ml)
    - [2.2 Δημιουργία υπολογιστικής μονάδας](#22-δημιουργία-υπολογιστικής-μονάδας)
    - [2.3 Φόρτωση των δεδομένων](#23-φόρτωση-των-δεδομένων)
    - [2.4 Δημιουργία Σημειωματάριων](#24-δημιουργία-σημειωματίων)
    - [2.5 Εκπαίδευση μοντέλου](#25-εκπαίδευση-μοντέλου)
      - [2.5.1 Ρύθμιση χώρου εργασίας, πειράματος, υπολογιστικού cluster και δεδομένων](#251-ρύθμιση-χώρου-εργασίας-πειράματος-υπολογιστικού-cluster-και-δεδομένων)
      - [2.5.2 Ρύθμιση AutoML και εκπαίδευση](#31-αποθήκευση-του-καλύτερου-μοντέλου)
  - [3. Ανάπτυξη μοντέλου και κατανάλωση endpoint με το Azure ML SDK](#33-κατανάλωση-endpoint)
    - [3.1 Αποθήκευση του καλύτερου μοντέλου](#πρόκληση)
    - [3.2 Ανάπτυξη μοντέλου](#κουίζ-μετά-το-μάθημα)
    - [3.3 Κατανάλωση endpoint](#ανασκόπηση-αυτοεκπαίδευση)
  - [🚀 Πρόκληση](#-challenge)
  - [Μετα-Διάλεξη κουίζ](#post-lecture-quiz)
  - [Ανασκόπηση & Αυτο-Μελέτη](#review--self-study)
  - [Ανάθεση εργασίας](#assignment)

## [Προ-Διάλεξη Κουίζ](https://ff-quizzes.netlify.app/en/ds/quiz/36)

## 1. Εισαγωγή

### 1.1 Τι είναι το Azure ML SDK;

Οι επιστήμονες δεδομένων και οι προγραμματιστές τεχνητής νοημοσύνης χρησιμοποιούν το Azure Machine Learning SDK για να δημιουργήσουν και να εκτελέσουν ροές εργασίας μηχανικής μάθησης με την υπηρεσία Azure Machine Learning. Μπορείτε να αλληλεπιδράσετε με την υπηρεσία σε οποιοδήποτε περιβάλλον Python, συμπεριλαμβανομένων των Jupyter Notebooks, Visual Studio Code ή του αγαπημένου σας IDE Python.

Βασικοί τομείς του SDK περιλαμβάνουν:

- Εξερεύνηση, προετοιμασία και διαχείριση του κύκλου ζωής των συνόλων δεδομένων που χρησιμοποιούνται σε πειράματα μηχανικής μάθησης.
- Διαχείριση πόρων στο cloud για παρακολούθηση, καταγραφή και οργάνωση των πειραμάτων μηχανικής μάθησης.
- Εκπαίδευση μοντέλων είτε τοπικά είτε με χρήση πόρων cloud, συμπεριλαμβανομένης της επιτάχυνσης εκπαίδευσης μοντέλων GPU.
- Χρήση αυτοματοποιημένης μηχανικής μάθησης, η οποία δέχεται παραμέτρους ρύθμισης και δεδομένα εκπαίδευσης. Αυτόματα επαναλαμβάνει αλγορίθμους και ρυθμίσεις υπερπαραμέτρων για να βρει το καλύτερο μοντέλο για την εκτέλεση προβλέψεων.
- Ανάπτυξη web υπηρεσιών για τη μετατροπή των εκπαιδευμένων μοντέλων σας σε RESTful υπηρεσίες που μπορούν να καταναλωθούν σε οποιαδήποτε εφαρμογή.

[Μάθετε περισσότερα για το Azure Machine Learning SDK](https://docs.microsoft.com/python/api/overview/azure/ml?WT.mc_id=academic-77958-bethanycheum&ocid=AID3041109)

Στο [προηγούμενο μάθημα](../18-Low-Code/README.md), είδαμε πώς να εκπαιδεύσουμε, να αναπτύξουμε και να καταναλώσουμε ένα μοντέλο με τρόπο Low code/No code. Χρησιμοποιήσαμε το σύνολο δεδομένων της Καρδιακής Ανεπάρκειας για να δημιουργήσουμε και ένα μοντέλο πρόβλεψης καρδιακής ανεπάρκειας. Σε αυτό το μάθημα, θα κάνουμε ακριβώς το ίδιο πράγμα αλλά χρησιμοποιώντας το Azure Machine Learning SDK.

![project-schema](../../../../translated_images/el/project-schema.420e56d495624541.webp)

### 1.2 Έργο πρόβλεψης καρδιακής ανεπάρκειας και εισαγωγή δεδομένων

Δείτε [εδώ](../18-Low-Code/README.md) την εισαγωγή στο έργο πρόβλεψης καρδιακής ανεπάρκειας και το σύνολο δεδομένων.

## 2. Εκπαίδευση μοντέλου με το Azure ML SDK
### 2.1 Δημιουργία χώρου εργασίας Azure ML

Για απλότητα, θα εργαστούμε σε ένα jupyter notebook. Αυτό συνεπάγεται ότι ήδη διαθέτετε έναν χώρο εργασίας και μια υπολογιστική μονάδα. Αν έχετε ήδη χώρο εργασίας, μπορείτε να μεταβείτε απευθείας στο τμήμα 2.3 Δημιουργία σημειωματίου.

Αν όχι, ακολουθήστε τις οδηγίες στην ενότητα **2.1 Δημιουργία χώρου εργασίας Azure ML** στο [προηγούμενο μάθημα](../18-Low-Code/README.md) για να δημιουργήσετε έναν χώρο εργασίας.

### 2.2 Δημιουργία υπολογιστικής μονάδας

Στο [Azure ML workspace](https://ml.azure.com/) που δημιουργήσαμε νωρίτερα, μεταβείτε στο μενού υπολογιστών και θα δείτε τους διάφορους διαθέσιμους πόρους υπολογισμού

![compute-instance-1](../../../../translated_images/el/compute-instance-1.dba347cb199ca499.webp)

Ας δημιουργήσουμε μια υπολογιστική μονάδα για να εφοδιάσουμε ένα jupyter notebook.
1. Κάντε κλικ στο κουμπί + Νέο.
2. Δώστε ένα όνομα στην υπολογιστική μονάδα σας.
3. Επιλέξτε τις επιλογές σας: CPU ή GPU, μέγεθος VM και αριθμό πυρήνων.
4. Πατήστε το κουμπί Δημιουργία.

Συγχαρητήρια, μόλις δημιουργήσατε μια υπολογιστική μονάδα! Θα χρησιμοποιήσουμε αυτή την υπολογιστική μονάδα για να δημιουργήσουμε ένα Σημειωματάριο στην [ενότητα Δημιουργία Σημειωματίων](#23-φόρτωση-των-δεδομένων).

### 2.3 Φόρτωση των δεδομένων
Ανατρέξτε στο [προηγούμενο μάθημα](../18-Low-Code/README.md) στην ενότητα **2.3 Φόρτωση των δεδομένων** αν δεν έχετε ανεβάσει ακόμα το σύνολο δεδομένων.

### 2.4 Δημιουργία Σημειωματίων

> **_ΣΗΜΕΙΩΣΗ:_** Για το επόμενο βήμα μπορείτε είτε να δημιουργήσετε ένα νέο σημειωματάριο από την αρχή, είτε μπορείτε να ανεβάσετε το [σημειωματάριο που δημιουργήσαμε](notebook.ipynb) στο Azure ML Studio σας. Για να το ανεβάσετε, απλώς κάντε κλικ στο μενού "Notebook" και ανεβάστε το σημειωματάριο.

Τα σημειωματάρια είναι ένα πολύ σημαντικό μέρος της διαδικασίας της επιστήμης δεδομένων. Χρησιμοποιούνται για να διεξάγουν εξερευνητική ανάλυση δεδομένων (EDA), να κάνουν κλήση σε ένα υπολογιστικό cluster για εκπαίδευση μοντέλου, να κάνουν κλήση σε ένα cluster για ανάπτυξη endpoint.

Για να δημιουργήσουμε ένα Σημειωματάριο, χρειαζόμαστε έναν κόμβο υπολογισμού που προσφέρει την υπηρεσία jupyter notebook. Επιστρέψτε στο [Azure ML workspace](https://ml.azure.com/) και κάντε κλικ στις Υπολογιστικές μονάδες. Στη λίστα των υπολογιστικών μονάδων θα δείτε την [υπολογιστική μονάδα που δημιουργήσαμε προηγουμένως](#22-δημιουργία-υπολογιστικής-μονάδας).

1. Στην ενότητα Εφαρμογές, κάντε κλικ στην επιλογή Jupyter.
2. Τσεκάρετε το κουτί "Ναι, καταλαβαίνω" και πατήστε το κουμπί Συνέχεια.
![notebook-1](../../../../translated_images/el/notebook-1.12998af7b02c83f5.webp)
3. Αυτό θα ανοίξει μια νέα καρτέλα περιηγητή με την υπηρεσία jupyter notebook όπως φαίνεται. Κάντε κλικ στο κουμπί "Νέο" για να δημιουργήσετε ένα σημειωματάριο.

![notebook-2](../../../../translated_images/el/notebook-2.9a657c037e34f1cf.webp)

Τώρα που έχουμε ένα Σημειωματάριο, μπορούμε να ξεκινήσουμε την εκπαίδευση μοντέλου με το Azure ML SDK.

### 2.5 Εκπαίδευση μοντέλου

Πρώτα απ' όλα, αν έχετε ποτέ αμφιβολία, ανατρέξτε στην [τεκμηρίωση του Azure ML SDK](https://docs.microsoft.com/python/api/overview/azure/ml?WT.mc_id=academic-77958-bethanycheum&ocid=AID3041109). Περιέχει όλες τις απαραίτητες πληροφορίες για να κατανοήσετε τα modules που θα δούμε σε αυτό το μάθημα.

#### 2.5.1 Ρύθμιση χώρου εργασίας, πειράματος, υπολογιστικού cluster και δεδομένων

Πρέπει να φορτώσετε το `workspace` από το αρχείο ρυθμίσεων χρησιμοποιώντας τον ακόλουθο κώδικα:

```python
from azureml.core import Workspace
ws = Workspace.from_config()
```

Αυτό επιστρέφει ένα αντικείμενο τύπου `Workspace` που αντιπροσωπεύει το χώρο εργασίας. Στη συνέχεια, πρέπει να δημιουργήσετε ένα `experiment` χρησιμοποιώντας τον ακόλουθο κώδικα:

```python
from azureml.core import Experiment
experiment_name = 'aml-experiment'
experiment = Experiment(ws, experiment_name)
```
Για να λάβετε ή να δημιουργήσετε ένα πείραμα από έναν χώρο εργασίας, ζητάτε το πείραμα χρησιμοποιώντας το όνομα του πειράματος. Το όνομα του πειράματος πρέπει να είναι 3-36 χαρακτήρες, να ξεκινά με γράμμα ή αριθμό και να περιέχει μόνο γράμματα, αριθμούς, κάτω παύλες και παύλες. Αν το πείραμα δεν βρεθεί στο χώρο εργασίας, δημιουργείται ένα νέο πείραμα.

Τώρα πρέπει να δημιουργήσετε ένα υπολογιστικό cluster για την εκπαίδευση με τον ακόλουθο κώδικα. Σημειώστε ότι αυτό το βήμα μπορεί να πάρει λίγα λεπτά.

```python
from azureml.core.compute import AmlCompute

aml_name = "heart-f-cluster"
try:
    aml_compute = AmlCompute(ws, aml_name)
    print('Found existing AML compute context.')
except:
    print('Creating new AML compute context.')
    aml_config = AmlCompute.provisioning_configuration(vm_size = "Standard_D2_v2", min_nodes=1, max_nodes=3)
    aml_compute = AmlCompute.create(ws, name = aml_name, provisioning_configuration = aml_config)
    aml_compute.wait_for_completion(show_output = True)

cts = ws.compute_targets
compute_target = cts[aml_name]
```

Μπορείτε να πάρετε το σύνολο δεδομένων από τον χώρο εργασίας χρησιμοποιώντας το όνομα του συνόλου δεδομένων ως εξής:

```python
dataset = ws.datasets['heart-failure-records']
df = dataset.to_pandas_dataframe()
df.describe()
```
#### 2.5.2 Ρύθμιση AutoML και εκπαίδευση

Για να ορίσετε τη ρύθμιση AutoML, χρησιμοποιήστε την [κλάση AutoMLConfig](https://docs.microsoft.com/python/api/azureml-train-automl-client/azureml.train.automl.automlconfig(class)?WT.mc_id=academic-77958-bethanycheum&ocid=AID3041109).

Όπως περιγράφεται στην τεκμηρίωση, υπάρχουν πολλές παράμετροι με τις οποίες μπορείτε να πειραματιστείτε. Για αυτό το έργο, θα χρησιμοποιήσουμε τις εξής παραμέτρους:

- `experiment_timeout_minutes`: Το μέγιστο χρονικό διάστημα (σε λεπτά) που επιτρέπεται να εκτελεστεί το πείραμα πριν σταματήσει αυτόματα και γίνουν διαθέσιμα τα αποτελέσματα.
- `max_concurrent_iterations`: Ο μέγιστος αριθμός ταυτόχρονων επαναλήψεων εκπαίδευσης που επιτρέπονται για το πείραμα.
- `primary_metric`: Το κύριο μέτρο που χρησιμοποιείται για να καθοριστεί η κατάσταση του πειράματος.
- `compute_target`: Ο στόχος υπολογισμού Azure Machine Learning για την εκτέλεση του πειράματος Αυτοματοποιημένης Μηχανικής Μάθησης.
- `task`: Ο τύπος εργασίας προς εκτέλεση. Οι τιμές μπορεί να είναι 'classification', 'regression' ή 'forecasting' ανάλογα με τον τύπο του προβλήματος αυτοματοποιημένης μηχανικής μάθησης που πρέπει να λυθεί.
- `training_data`: Τα δεδομένα εκπαίδευσης που θα χρησιμοποιηθούν εντός του πειράματος. Πρέπει να περιλαμβάνει τόσο τα χαρακτηριστικά εκπαίδευσης όσο και μια στήλη ετικέτας (προαιρετικά μια στήλη βαρών δείγματος).
- `label_column_name`: Το όνομα της στήλης ετικέτας.
- `path`: Η πλήρης διαδρομή προς το φάκελο του έργου Azure Machine Learning.
- `enable_early_stopping`: Αν θα ενεργοποιηθεί η πρώιμη διακοπή αν η βαθμολογία δεν βελτιώνεται σε σύντομο χρονικό διάστημα.
- `featurization`: Δείκτης για το αν το βήμα χαρακτηριστικής εξαγωγής θα γίνει αυτόματα ή όχι, ή αν θα χρησιμοποιηθεί προσαρμοσμένη χαρακτηριστική εξαγωγή.
- `debug_log`: Το αρχείο καταγραφής όπου θα γραφτούν πληροφορίες εντοπισμού σφαλμάτων.

```python
from azureml.train.automl import AutoMLConfig

project_folder = './aml-project'

automl_settings = {
    "experiment_timeout_minutes": 20,
    "max_concurrent_iterations": 3,
    "primary_metric" : 'AUC_weighted'
}

automl_config = AutoMLConfig(compute_target=compute_target,
                             task = "classification",
                             training_data=dataset,
                             label_column_name="DEATH_EVENT",
                             path = project_folder,  
                             enable_early_stopping= True,
                             featurization= 'auto',
                             debug_log = "automl_errors.log",
                             **automl_settings
                            )
```
Τώρα που έχετε τοποθετήσει τη ρύθμισή σας, μπορείτε να εκπαιδεύσετε το μοντέλο χρησιμοποιώντας τον ακόλουθο κώδικα. Αυτό το βήμα μπορεί να διαρκέσει έως και μία ώρα ανάλογα με το μέγεθος του cluster σας.

```python
remote_run = experiment.submit(automl_config)
```
Μπορείτε να εκτελέσετε το widget RunDetails για να δείτε τα διαφορετικά πειράματα.
```python
from azureml.widgets import RunDetails
RunDetails(remote_run).show()
```
## 3. Ανάπτυξη μοντέλου και κατανάλωση endpoint με το Azure ML SDK

### 3.1 Αποθήκευση του καλύτερου μοντέλου

Το `remote_run` είναι ένα αντικείμενο τύπου [AutoMLRun](https://docs.microsoft.com/python/api/azureml-train-automl-client/azureml.train.automl.run.automlrun?WT.mc_id=academic-77958-bethanycheum&ocid=AID3041109). Αυτό το αντικείμενο περιέχει τη μέθοδο `get_output()` που επιστρέφει την καλύτερη εκτέλεση και το αντίστοιχο προσαρμοσμένο μοντέλο.

```python
best_run, fitted_model = remote_run.get_output()
```
Μπορείτε να δείτε τις παραμέτρους που χρησιμοποιήθηκαν για το καλύτερο μοντέλο απλώς εκτυπώνοντας το fitted_model και να δείτε τις ιδιότητες του καλύτερου μοντέλου χρησιμοποιώντας τη μέθοδο [get_properties()](https://docs.microsoft.com/python/api/azureml-core/azureml.core.run(class)?view=azure-ml-py#azureml_core_Run_get_properties?WT.mc_id=academic-77958-bethanycheum&ocid=AID3041109).

```python
best_run.get_properties()
```

Τώρα, καταχωρίστε το μοντέλο με τη μέθοδο [register_model](https://docs.microsoft.com/python/api/azureml-train-automl-client/azureml.train.automl.run.automlrun?view=azure-ml-py#register-model-model-name-none--description-none--tags-none--iteration-none--metric-none-?WT.mc_id=academic-77958-bethanycheum&ocid=AID3041109).
```python
model_name = best_run.properties['model_name']
script_file_name = 'inference/score.py'
best_run.download_file('outputs/scoring_file_v_1_0_0.py', 'inference/score.py')
description = "aml heart failure project sdk"
model = best_run.register_model(model_name = model_name,
                                model_path = './outputs/',
                                description = description,
                                tags = None)
```
### 3.2 Ανάπτυξη μοντέλου

Μόλις αποθηκευτεί το καλύτερο μοντέλο, μπορούμε να το αναπτύξουμε με την κλάση [InferenceConfig](https://docs.microsoft.com/python/api/azureml-core/azureml.core.model.inferenceconfig?view=azure-ml-py?ocid=AID3041109). Η InferenceConfig αντιπροσωπεύει τις ρυθμίσεις για ένα προσαρμοσμένο περιβάλλον που χρησιμοποιείται για ανάπτυξη. Η κλάση [AciWebservice](https://docs.microsoft.com/python/api/azureml-core/azureml.core.webservice.aciwebservice?view=azure-ml-py) αντιπροσωπεύει ένα μοντέλο μηχανικής μάθησης που αναπτύσσεται ως endpoint web υπηρεσίας σε Azure Container Instances. Μια αναπτυγμένη υπηρεσία δημιουργείται από μοντέλο, script και συσχετιζόμενα αρχεία. Η προκύπτουσα web υπηρεσία είναι ένα ισορροπημένο HTTP endpoint με μια REST API. Μπορείτε να στείλετε δεδομένα σε αυτήν την API και να λάβετε την πρόβλεψη που επιστρέφεται από το μοντέλο.

Το μοντέλο αναπτύσσεται με τη μέθοδο [deploy](https://docs.microsoft.com/python/api/azureml-core/azureml.core.model(class)?view=azure-ml-py#deploy-workspace--name--models--inference-config-none--deployment-config-none--deployment-target-none--overwrite-false--show-output-false-?WT.mc_id=academic-77958-bethanycheum&ocid=AID3041109).

```python
from azureml.core.model import InferenceConfig, Model
from azureml.core.webservice import AciWebservice

inference_config = InferenceConfig(entry_script=script_file_name, environment=best_run.get_environment())

aciconfig = AciWebservice.deploy_configuration(cpu_cores = 1,
                                               memory_gb = 1,
                                               tags = {'type': "automl-heart-failure-prediction"},
                                               description = 'Sample service for AutoML Heart Failure Prediction')

aci_service_name = 'automl-hf-sdk'
aci_service = Model.deploy(ws, aci_service_name, [model], inference_config, aciconfig)
aci_service.wait_for_deployment(True)
print(aci_service.state)
```
Αυτό το βήμα θα πάρει λίγα λεπτά.

### 3.3 Κατανάλωση endpoint

Καταναλώνετε το endpoint σας δημιουργώντας ένα δείγμα εισόδου:
```python
data = {
    "data":
    [
        {
            'age': "60",
            'anaemia': "false",
            'creatinine_phosphokinase': "500",
            'diabetes': "false",
            'ejection_fraction': "38",
            'high_blood_pressure': "false",
            'platelets': "260000",
            'serum_creatinine': "1.40",
            'serum_sodium': "137",
            'sex': "false",
            'smoking': "false",
            'time': "130",
        },
    ],
}

test_sample = str.encode(json.dumps(data))
```
Και στη συνέχεια μπορείτε να στείλετε αυτήν την είσοδο στο μοντέλο σας για πρόβλεψη: 

```python
response = aci_service.run(input_data=test_sample)
response
```
Αυτό θα πρέπει να εξάγει `'{"result": [false]}'`. Αυτό σημαίνει ότι η είσοδος ασθενούς που στείλαμε στο endpoint παρήγαγε την πρόβλεψη `false` που σημαίνει ότι αυτό το άτομο πιθανότατα δεν θα παρουσιάσει καρδιακή προσβολή.

Συγχαρητήρια! Μόλις αξιοποιήσατε το μοντέλο που έχει αναπτυχθεί και εκπαιδευτεί στο Azure ML με το Azure ML SDK!

> **_ΣΗΜΕΙΩΣΗ:_** Μόλις ολοκληρώσετε το έργο, μην ξεχάσετε να διαγράψετε όλους τους πόρους.

## 🚀 Πρόκληση

 Υπάρχουν πολλά άλλα που μπορείτε να κάνετε μέσω του SDK, δυστυχώς δεν μπορούμε να τα δούμε όλα σε αυτό το μάθημα. Αλλά καλή είδηση, η εκμάθηση του πώς να περιηγηθείτε στην τεκμηρίωση του SDK μπορεί να σας βοηθήσει πολύ μόνοι σας. Ρίξτε μια ματιά στην τεκμηρίωση του Azure ML SDK και βρείτε την κλάση `Pipeline` που σας επιτρέπει να δημιουργείτε pipelines. Ένα Pipeline είναι μια συλλογή βημάτων που μπορούν να εκτελεστούν ως ροή εργασίας.

**ΥΠΟΔΕΙΞΗ:** Μεταβείτε στην [τεκμηρίωση του SDK](https://docs.microsoft.com/python/api/overview/azure/ml/?view=azure-ml-py?WT.mc_id=academic-77958-bethanycheum&ocid=AID3041109) και πληκτρολογήστε λέξεις-κλειδιά στη γραμμή αναζήτησης όπως "Pipeline". Θα πρέπει να βρείτε την κλάση `azureml.pipeline.core.Pipeline` στα αποτελέσματα αναζήτησης.

## [Κουίζ μετά το μάθημα](https://ff-quizzes.netlify.app/en/ds/quiz/37)

## Ανασκόπηση & Αυτοεκπαίδευση

Σε αυτό το μάθημα, μάθατε πώς να εκπαιδεύετε, να αναπτύσσετε και να χρησιμοποιείτε ένα μοντέλο για να προβλέψετε τον κίνδυνο καρδιακής ανεπάρκειας με το Azure ML SDK στο cloud. Δείτε αυτήν την [τεκμηρίωση](https://docs.microsoft.com/python/api/overview/azure/ml/?view=azure-ml-py?WT.mc_id=academic-77958-bethanycheum&ocid=AID3041109) για περαιτέρω πληροφορίες σχετικά με το Azure ML SDK. Προσπαθήστε να δημιουργήσετε το δικό σας μοντέλο με το Azure ML SDK. 

## Ανάθεση

[Έργο Data Science χρησιμοποιώντας το Azure ML SDK](assignment.md)

---

<!-- CO-OP TRANSLATOR DISCLAIMER START -->
**Αποποίηση ευθυνών**:
Αυτό το έγγραφο έχει μεταφραστεί χρησιμοποιώντας την υπηρεσία μετάφρασης με τεχνητή νοημοσύνη [Co-op Translator](https://github.com/Azure/co-op-translator). Ενώ επιδιώκουμε την ακρίβεια, παρακαλούμε να έχετε υπόψη ότι οι αυτοματοποιημένες μεταφράσεις ενδέχεται να περιέχουν λάθη ή ανακρίβειες. Το πρωτότυπο έγγραφο στη μητρική του γλώσσα πρέπει να θεωρείται η αυθεντική πηγή. Για κρίσιμες πληροφορίες, συνιστάται επαγγελματική ανθρώπινη μετάφραση. Δεν φέρουμε ευθύνη για τυχόν παρεξηγήσεις ή λανθασμένες ερμηνείες που προκύπτουν από τη χρήση αυτής της μετάφρασης.
<!-- CO-OP TRANSLATOR DISCLAIMER END -->