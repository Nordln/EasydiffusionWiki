ERROR: Exception:
Traceback (most recent call last):
  File "C:\stable-diffusion-ui\installer_files\env\lib\site-packages\pip\_vendor\urllib3\response.py", line 438, in _error_catcher
    yield
  File "C:\stable-diffusion-ui\installer_files\env\lib\site-packages\pip\_vendor\urllib3\response.py", line 561, in read
    data = self._fp_read(amt) if not fp_closed else b""
  File "C:\stable-diffusion-ui\installer_files\env\lib\site-packages\pip\_vendor\urllib3\response.py", line 527, in _fp_read
    return self._fp.read(amt) if amt is not None else self._fp.read()
  File "C:\stable-diffusion-ui\installer_files\env\lib\site-packages\pip\_vendor\cachecontrol\filewrapper.py", line 90, in read
    data = self.__fp.read(amt)
  File "C:\stable-diffusion-ui\installer_files\env\lib\http\client.py", line 458, in read
    n = self.readinto(b)
  File "C:\stable-diffusion-ui\installer_files\env\lib\http\client.py", line 502, in readinto
    n = self.fp.readinto(b)
  File "C:\stable-diffusion-ui\installer_files\env\lib\socket.py", line 669, in readinto
    return self._sock.recv_into(b)
  File "C:\stable-diffusion-ui\installer_files\env\lib\ssl.py", line 1241, in recv_into
    return self.read(nbytes, buffer)
  File "C:\stable-diffusion-ui\installer_files\env\lib\ssl.py", line 1099, in read
    return self._sslobj.read(len, buffer)
socket.timeout: The read operation timed out

During handling of the above exception, another exception occurred:

Traceback (most recent call last):
  File "C:\stable-diffusion-ui\installer_files\env\lib\site-packages\pip\_internal\cli\base_command.py", line 160, in exc_logging_wrapper
    status = run_func(*args)
  File "C:\stable-diffusion-ui\installer_files\env\lib\site-packages\pip\_internal\cli\req_command.py", line 247, in wrapper
    return func(self, options, args)
  File "C:\stable-diffusion-ui\installer_files\env\lib\site-packages\pip\_internal\commands\install.py", line 419, in run
    requirement_set = resolver.resolve(
  File "C:\stable-diffusion-ui\installer_files\env\lib\site-packages\pip\_internal\resolution\resolvelib\resolver.py", line 92, in resolve
    result = self._result = resolver.resolve(
  File "C:\stable-diffusion-ui\installer_files\env\lib\site-packages\pip\_vendor\resolvelib\resolvers.py", line 481, in resolve
    state = resolution.resolve(requirements, max_rounds=max_rounds)
  File "C:\stable-diffusion-ui\installer_files\env\lib\site-packages\pip\_vendor\resolvelib\resolvers.py", line 373, in resolve
    failure_causes = self._attempt_to_pin_criterion(name)
  File "C:\stable-diffusion-ui\installer_files\env\lib\site-packages\pip\_vendor\resolvelib\resolvers.py", line 213, in _attempt_to_pin_criterion
    criteria = self._get_updated_criteria(candidate)
  File "C:\stable-diffusion-ui\installer_files\env\lib\site-packages\pip\_vendor\resolvelib\resolvers.py", line 204, in _get_updated_criteria
    self._add_to_criteria(criteria, requirement, parent=candidate)
  File "C:\stable-diffusion-ui\installer_files\env\lib\site-packages\pip\_vendor\resolvelib\resolvers.py", line 172, in _add_to_criteria
    if not criterion.candidates:
  File "C:\stable-diffusion-ui\installer_files\env\lib\site-packages\pip\_vendor\resolvelib\structs.py", line 151, in __bool__
    return bool(self._sequence)
  File "C:\stable-diffusion-ui\installer_files\env\lib\site-packages\pip\_internal\resolution\resolvelib\found_candidates.py", line 155, in __bool__
    return any(self)
  File "C:\stable-diffusion-ui\installer_files\env\lib\site-packages\pip\_internal\resolution\resolvelib\found_candidates.py", line 143, in <genexpr>
    return (c for c in iterator if id(c) not in self._incompatible_ids)
  File "C:\stable-diffusion-ui\installer_files\env\lib\site-packages\pip\_internal\resolution\resolvelib\found_candidates.py", line 47, in _iter_built
    candidate = func()
  File "C:\stable-diffusion-ui\installer_files\env\lib\site-packages\pip\_internal\resolution\resolvelib\factory.py", line 206, in _make_candidate_from_link
    self._link_candidate_cache[link] = LinkCandidate(
  File "C:\stable-diffusion-ui\installer_files\env\lib\site-packages\pip\_internal\resolution\resolvelib\candidates.py", line 297, in __init__
    super().__init__(
  File "C:\stable-diffusion-ui\installer_files\env\lib\site-packages\pip\_internal\resolution\resolvelib\candidates.py", line 162, in __init__
    self.dist = self._prepare()
  File "C:\stable-diffusion-ui\installer_files\env\lib\site-packages\pip\_internal\resolution\resolvelib\candidates.py", line 231, in _prepare
    dist = self._prepare_distribution()
  File "C:\stable-diffusion-ui\installer_files\env\lib\site-packages\pip\_internal\resolution\resolvelib\candidates.py", line 308, in _prepare_distribution
    return preparer.prepare_linked_requirement(self._ireq, parallel_builds=True)
  File "C:\stable-diffusion-ui\installer_files\env\lib\site-packages\pip\_internal\operations\prepare.py", line 491, in prepare_linked_requirement
    return self._prepare_linked_requirement(req, parallel_builds)
  File "C:\stable-diffusion-ui\installer_files\env\lib\site-packages\pip\_internal\operations\prepare.py", line 536, in _prepare_linked_requirement
    local_file = unpack_url(
  File "C:\stable-diffusion-ui\installer_files\env\lib\site-packages\pip\_internal\operations\prepare.py", line 166, in unpack_url
    file = get_http_url(
  File "C:\stable-diffusion-ui\installer_files\env\lib\site-packages\pip\_internal\operations\prepare.py", line 107, in get_http_url
    from_path, content_type = download(link, temp_dir.path)
  File "C:\stable-diffusion-ui\installer_files\env\lib\site-packages\pip\_internal\network\download.py", line 147, in __call__
    for chunk in chunks:
  File "C:\stable-diffusion-ui\installer_files\env\lib\site-packages\pip\_internal\cli\progress_bars.py", line 53, in _rich_progress_bar
    for chunk in iterable:
  File "C:\stable-diffusion-ui\installer_files\env\lib\site-packages\pip\_internal\network\utils.py", line 63, in response_chunks
    for chunk in response.raw.stream(
  File "C:\stable-diffusion-ui\installer_files\env\lib\site-packages\pip\_vendor\urllib3\response.py", line 622, in stream
    data = self.read(amt=amt, decode_content=decode_content)
  File "C:\stable-diffusion-ui\installer_files\env\lib\site-packages\pip\_vendor\urllib3\response.py", line 587, in read
    raise IncompleteRead(self._fp_bytes_read, self.length_remaining)
  File "C:\stable-diffusion-ui\installer_files\env\lib\contextlib.py", line 131, in __exit__
    self.gen.throw(type, value, traceback)
  File "C:\stable-diffusion-ui\installer_files\env\lib\site-packages\pip\_vendor\urllib3\response.py", line 443, in _error_catcher
    raise ReadTimeoutError(self._pool, None, "Read timed out.")
pip._vendor.urllib3.exceptions.ReadTimeoutError: HTTPSConnectionPool(host='files.pythonhosted.org', port=443): Read timed out.