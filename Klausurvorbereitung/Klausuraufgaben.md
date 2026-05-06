# Klausuraufgaben

Automatisch aus den englischen Original-Wochenordnern extrahiert und ins Deutsche uebertragen.

## Week02_Preprocessing_ADC

### Week02_Preprocessing_ADC/01_InputSignals.ipynb

## Klausurvorbereitung

1) Es wird ein Quantisierer mit $w=16$ Bit verwendet. Bestimmen Sie die Datenmenge fuer 70 Minuten Aufnahme auf einer Audio-CD. Hinweis: Audio-CDs werden im Stereo-Modus aufgezeichnet.

2) Bestimmen Sie den Pegel in dB SPL eines Sinussignals mit einer Amplitude von $0.1$ Pa. Dieser Sinus wird zu einem digitalen Signal $x(n)=0.25\cdot\sin\left(2\pi f\frac{n}{r}\right)$ digitalisiert. Die maximal moegliche Amplitude des AD-Wandlers ist $A=1.0$. Bestimmen Sie den zugehoerigen Pegel in dB FS und den Kalibrierfaktor $a$.

3) Bestimmen Sie das SNR fuer ein Signal mit $-12$ dB FS bei Quantisierungsrauschen fuer $w=16$ Bit. Es gilt weiterhin $A=1.0$.

4) Gegeben ist ein Signal $x(t)=a\cdot\cos\left(2\pi ft\right)$ mit $f=2$ kHz. $x(t)$ hat einen Pegel von $75$ dB SPL. Bestimmen Sie den Parameter $a$. Ist es mit den gegebenen Informationen moeglich, das Vorzeichen von $a$ zu bestimmen? Bestimmen Sie den Pegel in dB SPL, wenn die Frequenz verdoppelt wird.

5) Welche Art von Funktion $y=f(x)$ fuehrt zu einem linearen Verlauf bei einer logarithmischen x-Achse, bei einer logarithmischen y-Achse und bei einer doppelt-logarithmischen Darstellung?

6) Ein Signal hat einen Kalibrierfaktor von $a=-120$ dB. Bestimmen Sie den Overload Point in dB SPL. Nehmen Sie an, dass das Signal ein Sinus ist.

7) Bestimmen Sie den Pegel des Quantisierungsrauschens in dB FS fuer $w=16$ Bit.

8) Geben Sie die mathematische Beschreibung eines digitalen Signals an, das dem hoechstmoeglichen Pegel in dB FS entspricht. Welcher Pegel in dB FS ergibt sich daraus?

9) Ein zeitkontinuierliches Signal $x(t)=\cos\left(7\cdot t\right)^2$ wird mit $r=10$ Hz abgetastet. Bestimmen Sie die ersten fuenf Samples.

10) Ein zeitdiskretes Signal mit Abtastrate $r=32$ kHz wird durch einen Tiefpass mit Grenzfrequenz $f_c=3400$ Hz gefiltert. Wie gross ist die kleinste notwendige Abtastfrequenz nach dem Tiefpass? Wie gross ist der maximal zulaessige ganzzahlige Downsampling-Faktor? Entspricht das Signal nach dem Tiefpass Wideband-Sprache oder Narrowband-Sprache?

11) Ein Mikrofonsignal $y(n)$ wird mit $r=48$ kHz aufgenommen. Anschliessend wird $y(n)$ mit einem Bandpass $h(n)$ mit den Grenzfrequenzen $f_1=100$ Hz und $f_2=7000$ Hz gefiltert: $z(n)=h(n)*y(n)$. Hat $z(n)$ einen DC-Anteil? Sind menschliche Stimmen in $z(n)$ verstaendlich? Welche hoechsten Frequenzen kommen in $y(n)$ und $z(n)$ vor?

12) Ein Signal $ð‘¥(ð‘¡)=\cosâ¡(500\cdot ð‘¡)$ wird mit $ð‘Ÿ=200$ Hz abgetastet. Fuehrt diese Abtastung zu Alias?

## Week03_Preprocessing_DiscreteFourierTransform

### Week03_Preprocessing_DiscreteFourierTransform/01_DiscreteFourierTransform.ipynb

## Klausurvorbereitung

1) Beweisen Sie die Symmetrie der DFT: $X(k) = X^*(K-k)$.

2) Ein Sinus mit $f=440$ Hz und Amplitude $\hat x = 1$ wird mit einer Abtastrate von $r=1$ kHz abgetastet. Bestimmen Sie die ersten drei Samples $x(n)$. Bestimmen Sie das Ergebnis der DFT ueber diese ersten drei Samples mit $N=K=3$. Bestimmen Sie die Energie im Zeitbereich und im Frequenzbereich.

3) Ein Signal hat eine Abtastrate von $r=48$ kHz. Die DFT verwendet eine Blocklaenge von $N=1000$ und eine Transformationslaenge von $K=1024$. Bestimmen Sie die Frequenzaufloesung $\Delta f$. Wird Zero Padding verwendet? Welcher Index $k$ entspricht $f=50$ Hz? Wie viele Indizes koennen nach der Transformation aufgrund der Symmetrie weggelassen werden?

4) Geben Sie eine Liste von Vor- und Nachteilen der DFT an.

5) Die z-Transformation kann zur Auswertung der Fourier-Transformation eines zeitdiskreten Signals durch folgende Ersetzung verwendet werden: $z\leftarrow e^{j2\pi f/r}$: $X(f)=\sum_{n=-\infty}^\infty x(n)\cdot e^{-j2\pi fn/r}$. Unter welchen Bedingungen ist die Ausgabe der DFT $X(k)=\sum_{n=0}^{N-1}x(n)\cdot e^{-j2\pi nk/N}$ identisch zur Fourier-Transformation eines zeitdiskreten Signals?

## Week04_Preprocessing_STFT

### Week04_Preprocessing_STFT/01_ShortTimeFourierTransform.ipynb

## Klausurvorbereitung

1) Ein Audiosignal der Laenge $3$ Sekunden hat eine Abtastrate von $r=16$ kHz. Die Frequenzaufloesung $\Delta f$ soll besser als $10$ Hz sein. Die Zeitaufloesung soll besser als $50$ Spektren pro Sekunde sein. Die Ueberlappung zweier benachbarter Fenster betraegt $50$ \%. Bestimmen Sie die minimalen Werte von $K$ und $N$. Ist Zero Padding notwendig? Bestimmen Sie den Speicherbedarf dieses Spektrogramms, wenn jeder reellwertige Parameter 4 Byte und jeder komplexwertige Parameter 8 Byte Speicher benoetigt.

2) Welche Aussage ist gemaess der oben dargestellten Spektrogramme richtig: Je kleiner die Fensterlaenge, desto besser die Zeitaufloesung eines Spektrogramms. Oder: Je groesser die Fensterlaenge, desto besser die Zeitaufloesung eines Spektrogramms.

3) Welche Aussage ist gemaess der oben dargestellten Spektrogramme richtig: Je kleiner die Fensterlaenge, desto besser die Frequenzaufloesung eines Spektrogramms. Oder: Je groesser die Fensterlaenge, desto besser die Frequenzaufloesung eines Spektrogramms.

4) Ein Audiosignal der Laenge $5$ Sekunden wird mit einer STFT analysiert. Die Fensterlaenge beziehungsweise Blockgroesse ist $N=100$ ms. Die Ueberlappung betraegt $75$ %. Wie viele Bloecke werden analysiert?

5) Ein Audiosignal der Laenge $5$ Sekunden wird mit einer STFT analysiert. Die Hopsize entspricht der Zeitaufloesung des menschlichen Ohrs. Die Spektren werden auf die Frequenzaufloesung des menschlichen Ohrs transformiert. Der im Spektrogramm gespeicherte Frequenzbereich ist $0\leq b \leq 24$ Bark. Wie viele Werte werden im Spektrogramm gespeichert?

6) Eine Fensterfunktion ist definiert durch $w(n)=\left(0.5-0.5\cdot\cos\left(2\pi\frac{n+0.5}{N}\right)\right)^\alpha$ mit $0\leq n<N$ und $0\leq\alpha$. Welche Hopsize fuehrt unabhaengig vom Parameter $\alpha$ zu einem konstanten Overlap-Add? Fuer welches $\alpha$ ist $w(n)$ gleich dem Hann-Fenster?

## Week05_Denoising_Bandpass

### Week05_Denoising_Bandpass/01_DiscreteFiltering.ipynb

## Klausurvorbereitung

1) Bestimmen Sie die [z-Transformation](../Basics/zTransform.ipynb) eines Filters $h(n)=[1, 2, 1]$. Ist dieser Filter ein Tiefpass, ein Bandpass oder ein Hochpass? Hinweis: Zur einfacheren Auswertung wird $r=1$ angenommen.

2) Wandeln Sie den FIR-Filter $h(n)=[1, 2, 1]$ in einen Hochpass um.

3) Bestimmen Sie die Faltung von $x(n) = [0, 1, 2]$ mit $h(n)=[1, 2, 1]$.

4) Bestimmen Sie die Samples der Impulsantwort eines FIR-Tiefpasses der Laenge $N=5$ bei einer Abtastrate von $r=1000$ Hz und einer Grenzfrequenz von $f_c = 250$ Hz.

5) Wie viele Multiplikationen und Additionen sind notwendig, um ein einzelnes Ausgangssample eines FIR-Filters mit der Laenge $N=501$ Samples zu berechnen?

6) Zeigen Sie, dass $a=\frac{\sum_n y\left(n-T\right)\cdot z(n)}{\sum_n y(n-T)^2}$ den Ausdruck $\sum_n \left(a\cdot y(n-T) - z(n)\right)^2$ minimiert.

7) Weisses Hintergrundrauschen hat naeherungsweise ein konstantes Leistungsdichtespektrum $\left|R(f)\right|^2\approx \text{const}$. Bestimmen Sie die Erhoehung des SNR bei Verwendung eines idealen FIR-Bandpasses mit Grenzfrequenzen $f_{c1}=100$ Hz und $f_{c2}=7000$ Hz, unter der Annahme, dass die menschliche Stimme diesen Filter ohne Qualitaetsverlust passieren kann. Die Abtastrate sei $r=48$ kHz.

8) Gegeben ist ein FIR-Tiefpass: $h(n)=[a,1,a]$ mit reellwertigem $a$. Fuer welche Werte von $a$ gilt die Bedingung $\left|H(f)\right| > 0$?

9) Gegeben ist ein FIR-Filter: $â„Ž(ð‘›)=[-1, 1]$. Ist $â„Ž(ð‘›)$ stabil? Geben Sie eine Begruendung fuer Ihre Antwort an. Bestimmen Sie den Realteil der Uebertragungsfunktion $ð»(ð‘“)$ von $â„Ž(ð‘›)$. Ist der Realteil fuer jedes $ð‘“$ positiv?

10) Gegeben ist ein Tiefpass $h(n)=[1, 4, 6, 4, 1]$. Die Abtastrate ist $r=48$ kHz. Bestimmen Sie die Impulsantwort des zugehoerigen Bandpasses mit $f_m=12$ kHz.

11) Fuer welche Werte von $a$ ist die folgende Gleichung stabil: $y(n) = a\cdot y(n-1) + (1-a)\cdot x(n)$?

12) Bestimmen Sie die Grenzfrequenz $f_c$ des in 11) gegebenen IIR-Filters in Abhaengigkeit vom Daempfungsparameter $a$.

13) Der Filter aus 11) hat die Impulsantwort $h(n) = (1-a) \cdot a^n$. Bestimmen Sie das kleinstmoegliche $n_0$, fuer das folgende Aussage gilt: $h(n_0) < h(n=0)\cdot e^{-5}$. Dieses $n_0$ kann als sinnvolle Laenge der Impulsantwort interpretiert werden. Fuer $n > n_0$ kann die Impulsantwort als stationaer interpretiert werden.

14) Ein Audio-Interface hat eine Abtastrate von $r=48$ kHz. Zur Entrauschung wird das Signal mit einem Bandpass mit Grenzfrequenzen $f_{c,1}=100$ Hz und $f_{c,2}=7$ kHz gefiltert. Hat das Audiosignal nach dem Filter einen Mittelwert von null? Kann menschliche Sprache diesen Filter passieren? Wuerde dieser Filter Netzbrummen bei $50$ Hz unterdruecken?

15) Bestimmen Sie die Pole und Nullstellen von $H(z)=\frac{z^2-4z-7}{z^2-9}$.

## Week06_Denoising_WienerFilter

### Week06_Denoising_WienerFilter/01_DenoiserWienerFilter.ipynb

## Klausurvorbereitung

1) Ist der vorgeschlagene Wiener-Filter $H(f)=\frac{\left|X(f)\right|^2}{\left|X(f)\right|^2 + \left|D(f)\right|^2}$ komplexwertig?

2) Bestimmen Sie den moeglichen Wertebereich von $H(f)$.

3) Skizzieren Sie den Wiener-Filter $H(f)$ fuer weisses Rauschen $\left|D(f)\right|^2=1$, $0<f<10$ und $X(f)=f$.

4) Skizzieren Sie das SNR in Abhaengigkeit von $f$ entsprechend den gegebenen Parametern aus Aufgabe 3).

5) Bei der Berechnung des Wiener-Filters wird eine kleine positive Zahl $\varepsilon=10^-16$ zum Nenner und zum Zaehler addiert. Warum?
