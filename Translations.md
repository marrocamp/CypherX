This page includes translations for the default messages included with xAuth. These translations are all user-created thus I am not responsible for their accuracy or updating them.
***
## Polish
<pre><code>join:
  register: '{RED}Nie jestes zarejestrowany.{NEWLINE}{RED}Zarejestruj sie wpisujac /register
    <haslo>.'
  login: '{RED}Zaloguj sie uzywajac polecenia /login <haslo>.'
  resume: '{BRIGHTGREEN}Witaj ponownie, twoja sesja logowania zostala wznowiona.'
  error:
    lockout: Zostales tymczasowo zablokowany z powodu przekroczonego limitu nieprawidlowych wprowadzen hasla.
    name: Twoj nick zawiera co najmniej jeden nieprawidlowy znak.
register:
  usage: '{RED}Poprawna formula: /register <haslo> [email]'
  success: '{BRIGHTGREEN}Zostales pomyslnie zarejestrowany!{NEWLINE}{BRIGHTGREEN}Teraz
    mozesz zalogowac sie uzywajac polecenia /login <haslo>'
  error:
    disabled: '{RED}Rejestracje sa w tej chwili wylaczone!'
    registered: '{RED}Jestes juz zarejestrowany!'
    limit: '{RED}Nie mozesz zarejestrowac wiekszej ilosci kont niz juz masz!'
    password: '{RED}Twoje haslo musi miec co najmniej {PWMINLENGTH} znakow!'
    email: '{RED}Uzyj poprawnego adresu email przy rejestracji!'
    general: '{RED}Cos poszlo nie tak przy tworzeniu twojego konta!'
login:
  usage: '{RED}Poprawna formula: /login <haslo>'
  success: '{BRIGHTGREEN}Jestes teraz zalogowany!'
  error:
    registered: '{RED}Nie jestes zarejestrowany!'
    authenticated: '{RED}Jestes juz zalogowany!'
    password: '{RED}Nieprawidlowe haslo!'
    active: '{RED}Twoje konto nie jest zaktywowane!'
    general: '{RED}Cos poszlo nie tak przy logowaniu cie!'
logout:
  success: '{BRIGHTGREEN}Zostales wylogowany!'
  error:
    logged: '{RED}Nie jestes zalogowany!'
    general: '{RED}Cos poszlo nie tak przy wylogowywaniu cie!'
changepw:
  usage: '{RED}Poprawna formulka: /changepw <stare haslo> <nowe haslo>'
  success: '{BRIGHTGREEN}Haslo zmienione!'
  error:
    disabled: '{RED}Zmiany hasel sa aktualnie wylaczone.'
    logged: '{RED}Nie jestes zalogowany!'
    incorrect: '{RED}Nieprawidlowe stare haslo!'
    invalid: '{RED}Twoje nowe haslo nie pasuje do wymagan zlozonosci hasla!'
    general: '{RED}Cos poszlo nie tak przy zmianie twojego hasla!'
authurl:
  registration: '{RED}Rejestracja AuthURL jest wylaczona.'
  changepw: '{RED}AuthURL nie zezwala na zmiany hasel.'
misc:
  illegal: '{GRAY}Musisz byc zalogowany, by to zrobic!'
  timeout: Zalogowanie sie zajelo ci za duzo czasu!
  strikeout: Wpisales zle haslo zbyt wiele razy!
  reloaded: '{RED}Serwer przeladowany, musisz sie zalogowac.'
admin:
  permission: Nie masz zezwolenia na uzycie tej komendy!
  register:
    usage: '{RED}Poprawna formula: /xauth register <nick> <haslo> [email]'
    success: '{BRIGHTGREEN}Konto pomyslnie stworzone dla: {WHITE}{TARGET}'
    error:
      registered: '{RED}Ten gracz jest juz zarejestrowany!'
      general: '{RED}Cos poszlo nie tak przy tworzeniu konta dla {TARGET}'
  changepw:
    usage: '{RED}Poprawna formula: /xauth changepw <nick> <nowe haslo>'
    success: 'Haslo {TARGET} {BRIGHTGREEN}zostalo zmienione!'
    error:
      registered: '{RED}Ten gracz nie jest zarejestrowany!'
      general: '{RED}Cos poszlo nie tak przy zmianie hasla {TARGET}!'
  logout:
    usage: '{RED}Poprawna formula: /xauth logout <nick>'
    error:
      logged: '{TARGET} {RED}nie jest zalogowany!'
      general: '{RED}Cos poszlo nie tak przy wylogowywaniu tego gracza!'
    success:
      player: '{TARGET} {BRIGHTGREEN}zostal wylogowany!'
      target: '{BRIGHTGREEN}Zostales wylogowany przez administratora!'
  unregister:
    usage: '{RED}Poprawna formula: /xauth unregister <nick>'
    error:
      registered: '{RED}Ten gracz nie jest zarejestrowany!'
      general: '{RED}Cos poszlo nie tak przy wyrejestrowywaniu tego gracza!'
    success:
      player: '{TARGET} {BRIGHTGREEN}zostal wyrejestrowany!'
      target: '{RED}Zostales wyrejestrowany i wylogowany!'
  location:
    usage: '{RED}Poprawna formula: /xauth location set|remove [global]'
    set:
      error:
        global: '{RED}Globalne miejsce teleportacji jest przydzielone temu swiatu.{NEWLINE}{RED}Prosze
          najpierw je usunac.'
        general: '{RED}Cos poszlo nie tak przy ustawianiu tego miejsca!'
      success:
        regular: '{BRIGHTGREEN}Miejsce teleportacji dla tego swiata zostalo ustawione na twoja lokacje!'
        global: '{BRIGHTGREEN}Globalne miejsce teleportacji zostalo ustawione na twoja lokacje!'
    remove:
      error:
        noglobal: '{RED}Globalne miejsce teleportacji nie jest ustawione!'
        notset: '{RED}Ten swiat nie ma miejsca teleportacji!'
        global: '{RED}Globalne miejsce teleportacji jest ustawione na tym swiecie.{NEWLINE}{RED}Prosze o
          uzycie /xauth location remove global'
        general: '{RED}Cos poszlo nie tak przy usuwaniu tego miejsca!'
      success:
        regular: '{BRIGHTGREEN}Miejsce teleportacji dla tego swiata zostalo usuniete!'
        global: '{BRIGHTGREEN}Globalne miejsce teleportacji zostalo usuniete!'
  reload: '{BRIGHTGREEN}xAuth przeladowany.'
  activate:
    usage: '{RED}Poprawna formula: /xauth activate <nick>'
    error:
      registered: '{RED}Ten gracz nie jest zarejestrowany!'
      active: '{RED}Ten gracz zostal juz aktywowany!'
      general: '{RED}Cos poszlo nie tak przy aktywacji tego gracza!'
    success: '{BRIGHTGREEN}{TARGET} zostal aktywowany!'
  config:
    usage: '{RED}Poprawna formula: /xauth config <wezel> <wartosc>'
    error:
      exist: '{RED}Ten wezel konfiguracji nie istnieje!'
      int: '{RED}Ten wezel konfiguracji wymaga liczby calkowitej!'
      invalid: '{RED}To ustawienie nie moze zostac zmienione z uzyciem tej komendy!'
    success: '{BRIGHTGREEN}Konfiguracja zaktualizowana!'</code></pre>