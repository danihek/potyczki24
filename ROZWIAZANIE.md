# Jesteśmy Teamem number 22 (Jakub Gawęda, )

# Zadanie 1
 * Według opisu

# Zadanie 2
Instalacja longhorna podazajac https://longhorn.io/
Doinstalowanie yamla iscsi z repo ranchera z githuba

# Zadanie 3
 * Instalacja tetrisa z repo, dostępny w APPS

# Zadanie 6
Aby zachować PersistentVolume i ponownie podłączyć go do Deploymentu po jego 
wygaśnięciu i wznowieniu, można skorzystać z mechanizmu PVC (PersistentVolumeClaim) 
w Kubernetes. W tym celu można skonfigurować PVC wraz z Deploymentem, który 
używa tego PVC. Następnie, gdy Deployment jest skalowany do 0, PVC pozostaje 
zachowany, a PersistentVolume jest nadal związany z PVC. Po ponownym wznowieniu 
Deploymentu, PVC będzie próbować ponownie związać się z PersistentVolume, 
który został zachowany. Przykład znaleźć można w pliku (przyklad_1.yaml).
W powyższym przykładzie, PersistentVolumeClaim (PVC) o nazwie "moj-pvc" jest 
zdefiniowany, który ma za zadanie żądać zasobu dyskowego o rozmiarze 1Gi. 
Następnie Deployment "moj-deployment" używa tego PVC poprzez wolumin, który 
jest montowany do kontenera w ścieżce "/moje-dane". Gdy Deployment jest 
wygaszany, PVC pozostaje zachowany. Po wznowieniu Deploymentu, PVC ponownie 
próbuje związać się z PersistentVolume, który został zachowany, umożliwiając 
zachowanie danych.
Zapewnienie, że PersistentVolume zostanie zachowany i ponownie podłączony 
po wznowieniu Deploymentu, wymaga odpowiedniej konfiguracji PVC oraz zgodnego 
ustawienia Deploymentu z woluminem używającym PVC.

# Zadanie 7
Adrianie, istnieją dwie główne metody, aby znaleźć YAML dla istniejącego 
zasobu w klastrze Kubernetes:

 * Użyj komendy kubectl get: Możesz użyć polecenia `kubectl get` do 
wylistowania zasobów w klastrze. Następnie możesz użyć komendy `kubectl 
get <rodzaj_zasobu> <nazwa_zasobu> -o yaml`, aby uzyskać YAML dla 
konkretnego zasobu. Na przykład, jeśli chcesz uzyskać YAML dla zasobu 
Deployment o nazwie "my-deployment", wykonaj: `kubectl get deployment 
my-deployment -o yaml`.

 * Użyj narzędzia do eksportu: Możesz także skorzystać z narzędzi 
do eksportu konfiguracji klastra, takich jak `kubectl` z pluginem `krew`, 
który umożliwia eksportowanie YAML dla wszystkich zasobów w klastrze. 
Po zainstalowaniu pluginu, możesz użyć komendy `kubectl krew export 
all -o yaml > plik.yaml`, aby wyeksportować konfigurację wszystkich 
zasobów do pliku YAML.

Pamiętaj, że obie metody są równie skuteczne, ale wybierz tę, która lepiej odpowiada twoim potrzebom i preferencjom.

# Zadanie 7.5
Uruchomienie kontenera MySQL na najprostszych domyślnych ustawieniach 
nie jest zalecane z punktu widzenia bezpieczeństwa i wydajności. 
Domyślne ustawienia mogą być podatne na ataki, takie jak brute force 
czy SQL injection, oraz nie zapewniają optymalnych parametrów wydajnościowych 
dla konkretnej aplikacji. Zamiast tego, zaleca się skonfigurowanie 
MySQL zgodnie z zasadami bezpieczeństwa, takimi jak wykorzystanie silnych 
haseł, ograniczenie dostępu do bazy danych, zabezpieczenie przed atakami 
DDoS oraz optymalizacja parametrów wydajnościowych w zależności od potrzeb 
aplikacji. Sugestia poprawy: Skonfigurowanie MySQL zgodnie z najlepszymi 
praktykami bezpieczeństwa oraz optymalizacji wydajności, takimi jak 
ustawienie silnych haseł, ograniczenie dostępu do bazy danych za pomocą 
użytkowników i uprawnień, oraz dostosowanie parametrów konfiguracyjnych 
do wymagań aplikacji.

# Zadanie 8
W Kubernetes, resource o nazwie Gateway jest używany do zarządzania 
dostępem do aplikacji uruchomionych w klastrze. Jest to rodzaj obiektu, 
który kontroluje przekierowania ruchu sieciowego do usług wewnątrz 
klastra na podstawie określonych reguł i konfiguracji. Gateway 
umożliwia kontrolę, jak ruch sieciowy jest kierowany do różnych 
usług w klastrze, co pozwala na elastyczne zarządzanie ruchem i 
bezpieczeństwem aplikacji.

# Zadanie 9
Resource w Kubernetes, takie jak Deployment, jest odpowiedzialne 
za definiowanie i zarządzanie deklaratywnym stanem aplikacji, 
obejmującym ReplicaSets, które zarządzają replikami podów. ReplicaSet 
natomiast zapewnia kontrolę nad liczbą replik podów w klastrze, 
wskazując na konkretne obrazy kontenerów. Deployment natomiast 
dostarcza funkcjonalności rolowania aktualizacji, 
cofania zmian i zarządzania cyklem życia aplikacji.

# Zadanie 11
Uzytkownicy oraz ich hasla:
muhammed_yassuff: pECjNBZ15Q92oFYe <- Dyrektor IT
muhhamad_yussuff: YZQC8r6zYfQng0MS <- Stażysta
