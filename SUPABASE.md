# Configurazione della raccolta risultati

Il gioco funziona anche senza database. Per raccogliere i risultati anonimi e
usarli nell'area docente:

1. Creare un progetto gratuito su <https://supabase.com/dashboard>.
2. Aprire **SQL Editor**, incollare ed eseguire `supabase-setup.sql`.
3. In **Authentication > Users**, creare l'utente docente con e-mail e password.
4. Copiare l'UUID dell'utente e, nel SQL Editor, eseguire:

   ```sql
   insert into public.admin_users (user_id)
   values ('UUID-UTENTE-DOCENTE');
   ```

5. In **Project Settings > API**, copiare:
   - Project URL;
   - chiave pubblica `anon` / `publishable`.
6. Inserire entrambi i valori in `config.js`. La chiave pubblica può essere
   esposta nel browser: la protezione è affidata alle policy RLS. Non inserire
   mai la `service_role` key.
7. In **Authentication > URL Configuration**, aggiungere:
   `https://angelamicocci-rgb.github.io/pensiero-critico-ai/admin.html`

Questa URL è necessaria anche per il pulsante **Password dimenticata?**. Il link
ricevuto via e-mail riporta all'area docente, dove viene mostrato il modulo per
impostare la nuova password.

## Privacy

- Usare solo nickname o codici anonimi.
- Non chiedere nomi, e-mail degli studenti o risposte libere contenenti dati personali.
- Informare gli studenti della finalità e del periodo di conservazione.
- Eliminare i risultati al termine dell'attività o secondo la policy scolastica.
- Valutare con il responsabile privacy della scuola base giuridica, informativa
  e misure richieste prima dell'uso con minori.
